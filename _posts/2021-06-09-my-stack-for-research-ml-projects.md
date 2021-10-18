---
layout: post
title: "My stack for research ML projects"
author: Patrick Mineault
date: 2021-06-09
categories: ml/ai/nlp
tags: best-practice
---
[https://xcorr.net/2021/06/09/my-stack-for-research-ml-projects/](https://xcorr.net/2021/06/09/my-stack-for-research-ml-projects/)

> - The [Full Stack Deep Learning](https://fullstackdeeplearning.com/) class from Berkeley is a good place to learn how to organize deep learning projects. I had originally intended to go all-in on cloud infra to run models and analyze data. The class makes a solid argument that it ends being cheaper to build your own machine for local testing, then scale on the cloud as needed.

> - I used an ad-hoc project folder structure inspired by [PyRSE](https://merely-useful.tech/py-rse/index.html). Elizabeth DuPre told me about cookiecutter, which allows one to create projects from templates. [I ended up using the **datascience cookiecutter**](https://drivendata.github.io/cookiecutter-data-science/) for a subset of the project, and generally I liked it (although it is a bit too nested for my taste).

> - I’ve used TF in the past, but I decided to use PyTorch this round, since a lot of the models I wanted to test were released in PyTorch. The PyTorch documentation is excellent. A surprising chunk of my codebase ended up being training loops, so for next time I will consider [PyTorch Lightning](https://www.pytorchlightning.ai/).

> - I ended up instead using **Weights and Biases** (wandb). In your code, you push your results along with metadata to their server using a simple library that you can pip install. The library takes care of adding the git hash to the payload so you know what code generated the result. You can also use the libary to send and store weights, images, checkpoints, etc. You get a fully customizable dashboard built on vega-lite to keep track of your results.
>   - https://docs.wandb.ai/guides/data-vis/log-tables
>   - https://docs.wandb.ai/ref/app/features/custom-charts
