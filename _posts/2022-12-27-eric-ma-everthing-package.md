---
layout: post
title: "Everything gets a package? Yes, everything gets a package"
author: Eric Ma
date: 2022-03-31
categories: data
tags: best-practice
---

[https://ericmjl.github.io/blog/2022/3/31/everything-gets-a-package-yes-everything-gets-a-package/](https://ericmjl.github.io/blog/2022/3/31/everything-gets-a-package-yes-everything-gets-a-package/) 

> ## But why all the trouble?
>
> Isn't there a *ton* of overhead that comes from doing software work? You now suddenly have to manage dependencies, start documenting your functions, add tests... you suddenly can't just store data with code in the repo... I can't just commit the notebook and be done with it?
>
> Let me explain. Data science is no longer solo work, but teamwork. The corollary is this: *discipline enables better collaborative work*. Have you encountered the following issues?
>
> - A notebook that works on your colleague's computer trips up on imports?
> - A notebook that ran on your colleague's machine errors out because you were missing a data file?
> - Your PyMC model definition doesn't agree with your colleagues', because you two were independently editing two notebooks that now each contains drifted model code?
>
> ## Optimize for standardized structure
>
> [Cookiecutter Data Science by DrivenData](https://drivendata.github.io/cookiecutter-data-science/) was the OG inspiration for this idea. Basically, I ensure that every project I work on starts with a standardized project directory structure that looks, at the minimum, something like this:
>
> ```
> andorra_geospatial/  # the project name
> |- docs/
> |- notebooks/
> |- andorra_geospatial/  # custom source code, usually named after the project name.
> |- tests/
> |- .gitignore
> |- .pre-commit-config.yaml
> |- environment.yml
> |- pyproject.toml
> |- setup.cfg
> |- setup.py
> ```
>
> If you squint hard, you'll notice that the project structure essentially looks like a Python software package, except that there is also a `notebooks/` directory added into the mix. This is intentional! Structuring every project in this fashion ensures that when future me, or someone else comes to view the project repository, they know exactly where to go for code artifacts.
>
> Need an analysis? Look it up in `notebooks/`. Need to find where that function was defined? Look it up in `andorra_geospatial` submodules. Need to add a package? Update the `environment.yml` definition and get `conda` or `mamba` to update your environment. Imposing this structure ensures your code is organized, and as the CCDS website states: `Well organized code tends to be self-documenting in that the organization itself provides context for your code without much overhead.`
>
> But what about a `data/` directory? That's a good question - lots of people store CSV files in a `data/` directory. If working in a professional setting, it is becoming increasingly idiomatic to pull data from a single source of truth, such as an PostgreSQL database or an S3 bucket, rather than caching a local copy. At work at Moderna, we have an awesome single source of truth for versioned datasets from which we pull data programmatically into our projects via a Python client. (The data is cached locally but not in our repo -- it is cached in a special directory in our home folder.) 

> ## Optimize for effective processes and habits
>
> ### Follow the 1-to-1-to-1-to-1... rule
>
> No matter how big or small, every project gets a `git` repository on some hosted service, whether GitHub (my favourite) or Bitbucket. Doing so ensures that my code can always be pulled into a new machine from a *single source of truth.* That project also gets one conda environment associated with it, one custom source package associated with it, one single source of truth documentation, and one continuous integration pipeline. In other words, there is always a 1:1 mapping from project to all of the digital artifacts present in the project, and there is a single source of truth for everything. [I detail more in my Data Science Bootstrap Notes page on the rule of one-to-one](https://ericmjl.github.io/data-science-bootstrap-notes/follow-the-rule-of-one-to-one-in-managing-your-projects/).
>
> ### Commit code often
>
> By committing code often, I get the benefit of history in the git log! I can think about the number of times I accidentally deleted a chunk of notebook code that I needed later, and how the git history helped me recover that code chunk.
>
> ### Ensure code adheres to minimum quality standards
>
> All code that I write (that gets placed in the custom source code directory) should, at the minimum, have a docstring attached to it. I try to go one step further and ensure that they have type hints (which are *incredibly* useful!) and an example-based test associated with it. Even better is if the docstring contains a minimum working example of how to use the chunk of code!
>
> ### Refactor by using source `.py` files
>
> Like any other user of Jupyter notebooks as prototyping environments, functions I write in the notebook may end up relying on the internal state of the notebook. **The cleanest way to ensure that a block of code operates independently of the internal state of the notebook is to cut and paste it out into a `.py` file, and then re-import the function back into the notebook.** This is refactoring, data science-style. By cutting and pasting functions out, I'm forced to account for every variable inside the function.
>
> ### Pre-define with colleagues what a unit of work will look like
>
> When doing team data science, communication and coordination are key. Usually, there are *independent units of work* that need to be completed by individuals, and at times these units of work can run in parallel. Some examples of these include:
>
> 1. Software-oriented pieces of work, such as contributing new functions to the custom library,
> 2. Analyses using the same code but on different datasets,
>
> In each case, it is highly advantageous for you, the data scientist, to pre-define with your teammates what a unit of work looks like and agree upon the boundaries of the unit of work. If you find stuff out of scope, such as programming style issues that bug you, it's important to rein in the desire to "just make the change". Raise the issue with them, find a place to record the issue, and stay within the bounds of your agreed-upon unit of work. Use a new pull request to fix that issue so that the pull request doesn't grow unmanageably large.

> ## Optimize for automation
>
> Once your processes are well-defined, automation becomes a cinch! The value of automation is obvious - you save time and effort! *But the value of automation can only be realized when your processes are also stabilized*

