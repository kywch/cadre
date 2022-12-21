---
layout: post
title: "Everything gets a package: My python data science setup"
author: Ethan Rosenthal
date: 2022-02-01
categories: data
tags: [analytics, best-practice]
---

[https://www.ethanrosenthal.com/2022/02/01/everything-gets-a-package/](https://www.ethanrosenthal.com/2022/02/01/everything-gets-a-package/)

> I used GitHub as the place to store my code and notebooks. Data all lived in cloud storage. A python package for my code held all of the python dependencies. It turn out, being forced to make your code portable is the same thing as requiring reproducibility in building and running your code. It’s nice when constraints incentivize best practices.
>
> I use [pyenv](https://github.com/pyenv/pyenv) to manage the exact version of Python that I use for each project. I pair `pyenv` with [pyenv-virtualenv](https://github.com/pyenv/pyenv-virtualenv) in order to use `pyenv` for managing both my python version and my virtual environments. When I start a new project, I first create a virtual environment with a specific version of Python:
>
> The nice thing about `poetry` is that it allows me to easily “graduate” my code from notebook to script to package. In the notebook phase, `poetry` allows me to recreate the virtual environment that ran the notebook. If I want to move my code out of the notebook and into a full-fledged package, that’s a small lift if I’ve been using `poetry` the whole time.
>
> Speaking of the package, I put my code inside of a `src/` directory because of [this blog post](https://hynek.me/articles/testing-packaging/). I name my package the same name as the directory which is the same name as the virtual environment. For whatever reason, I often uses dashes for the latter two and underscores for the package.
