---
layout: post
title: "How to use Jupyter Notebooks in 2020"
author: LJ Miranda
date: 2020-03-16
categories: data
tags: best-practice
---
[https://ljvmiranda921.github.io/notebook/2020/03/16/jupyter-notebooks-in-2020-part-2/](https://ljvmiranda921.github.io/notebook/2020/03/16/jupyter-notebooks-in-2020-part-2/)

> **Principles**

> 1. Keep a standard project structure and gitflow. I highly-recommend adopting cookiecutter-datascience. By setting a project structure at the very start, you already open the idea for collaboration. Lastly, I encourage that researchers learn gitflow and use some of the tools here to facilitate better collaboration.

> 2. Refactor oft-repeated functions into Python modules. Most of the time, we have functions for loading data, creating charts, or cleaning dataframes that are scattered throughout multiple notebooks. If possible, we can refactor them into Python modules so that we can import them many times. This also helps in turning your exploratory notebooks into production ones in the long-run.

> 3. Ensure that your notebook runs from top-to-bottom. Although Notebooks provide the flexibility to rearrange cells however we want, it becomes a nuisance when the notebook is not ours! This principle requires some discipline: after your analysis, ensure that your notebook runs correctly (doesn’t spit out an error, gives more-or-less the expected results) when clicking “Restart Kernel and Run All.” Once you get past this initial slump, you’re on your way to turning your Notebooks into production-ready onesONnce you get past this initial slump, you’re on your way to turning your Notebooks into production-ready ones.

> 4. For data pipelines, use papermill and configure your notebook to take advantage of it. Papermill is a life-changer. Once I’m done with Principle#3, what I’d do is [parametrize my notebooks](https://github.com/nteract/papermill#parameterizing-a-notebook), create a [config file](https://github.com/nteract/papermill#execute-via-cli) based on these parameters, and rerun these notebooks with the config file as input. It’s so powerful that it can be the bread-and-butter in your project lifecycle from exploration to production!

> **My wishlist, just three:**

> * Make “Restart Kernel and Run All” (RKRA) a first-class citizen I always think of RKRA, loosely, like a compiler: first it inspects if the logic flow of your notebook checks out, and transforms it into a readable material. Whenever I hit RKRA and it “passes,” then I have a certain level of confidence that I don’t have undeclared variables, unordered rows, or unimported libraries. I hope that RKRA can be displayed more prominently in the interface.

> * More Notebook IDEs The tool nbdev seems to be a good leap forward, but I hope that there would be more players in this space. We have discussed various tools like nbstripout and nbdime, and I hope that there’s an IDE (or an opinionated Jupyter “distribution”) that ships this right off the bat. Perhaps Jupyter Notebooks can be treated as “editors” with easily-customizable configs, and us developers can just save and share our configs like in tmux or vim. It would be fun looking at other’s configs that way!

> * A cell-lock mode? The ability to order cells freely is both bane and boon. On one hand, it allows me to switch context and be more flexible in how I organize my cells. On the other, it facilitates misuse and discourage software best practices. I wish that there’s a simple toggle to enable a cell-lock mode, where I’m not allowed to move cells back and forth and force me in a linear workflow.
