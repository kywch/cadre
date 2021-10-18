---
layout: post
title: "6 steps for leading successful data science teams"
author: Rama Ramakrishnan
date: 2021-08-16
categories: Data, Teamwork
tags: [leadership, best-practice]
---
[https://mitsloan.mit.edu/ideas-made-to-matter/6-steps-leading-successful-data-science-teams](https://mitsloan.mit.edu/ideas-made-to-matter/6-steps-leading-successful-data-science-teams)

> **1. Point data science teams toward the right problem.**
> More generally, to maximize the chance of identifying the right problem, look at what other companies in your industry are doing, especially early adopters of data science. Pay less attention to *how* they are solving it, as there are usually many different ways to solve any data science problem, and more attention to *what* they are solving.

> **2. Decide on a clear evaluation metric up front.**
> To solve a problem, data science teams typically build lots of models and then select the one that seems best. To make this selection they need a metric. Given multiple models, they can use this metric to rank them and pick the best one.
>
> Leaders need to use business judgment to determine what that metric should be, which is trickier than it sounds. In any complex business situation, there’s no single perfect metric. There are usually many relevant metrics and they often conflict with one another.

> **3. Create a common-sense baseline first.**
> Once you’ve decided on a relevant, important problem and defined a clear evaluation metric that reflects business priorities, you need to create a common-sense baseline, which is how your team would solve the problem if they didn’t know any data science. For example, if your data science team is building a personalized recommendation algorithm for your e-commerce site, a simple baseline would be tracking what product categories visitors look at, and recommending best-selling products from those categories.
>
> Building a common-sense baseline will force the team to get the end-to-end data and evaluation pipeline working and uncover any issues, such as with data access, cleanliness, and timeliness. It will also surface any tactical obstacles with actually calculating the evaluation metric.
>
> Knowing how well the baseline does on the evaluation metric will give a quick ballpark idea of how much benefit to expect from the project. Experienced practitioners know all too well that common-sense baselines are often hard to beat. And even when data science models beat these baselines, they may do so by slim margins.
>
> Finally, this also leads the data science team to spend some time thinking about the data and the problem from first principles, rather than just diving in and throwing powerful machine learning models at the problem.

> **4. Manage data science projects more like research than like engineering.**
> There’s a strong element of research in most data science work, which means a fair amount of time spent on dead ends with nothing to show for the effort. This trial and error makes it hard to predict when a breakthrough will occur.
>
> For example, data scientists may be able to quickly produce a solution that’s 6% better. But they can’t predict how long it will take them to get from 6% to 10% better. It may happen tomorrow, it may happen next month, it may never happen.

> **5. Check for ‘truth and consequences.’**
> It is important to subject results to intense scrutiny to make sure the benefits are real and there are no unintended negative consequences. The most basic check is making sure the results are calculated on data that was not used to build the models.
>
> Assuming the results are real, also check that there are no adverse side effects. When a model improves performance on a selected metric, it may do so at the expense of other important metrics. For example, an e-commerce business may focus on improving revenue per visitor with an improved recommendation algorithm. Revenue per visitor is the product of conversion rate and revenue per conversion.

> **6. Log everything, and retrain periodically.**
> And over time, the nature of the data being fed to the model will start to drift away from the data used to build the model. If no action is taken, this will reduce the efficacy of the model, so it is important to make sure that data science teams have automated processes in place to track model performance over time and retrain as necessary.
>
> Data science models, like software in general, tend to require a great deal of future effort because of the need for maintenance and upgrades.