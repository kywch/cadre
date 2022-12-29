---
layout: post
title: "Lessons from deploying deep learning to production"
author: Peter Gao
date: 2022-05-16
categories: ml/ai/nlp
tags: [best-practice, mlops]
---

[https://thegradient.pub/lessons-from-deploying-deep-learning-to-production/](https://thegradient.pub/lessons-from-deploying-deep-learning-to-production/)

> It took only a few weeks to hack together the first version of the model. Then another 6 months to ship a new and improved version of the model. And as we worked more on some of the pieces (better labeling infrastructure, cloud data processing, training infrastructure, deployment monitoring) we were able to retrain and redeploy models about every month to every week. As we set up more model pipelines from scratch and worked on improving them, we began to see some common themes. Applying our learnings to the new pipelines, it became easier to ship better models faster and with less effort.
>
> So to recap: in research and prototyping stages, the focus is on building and shipping a model. But as a system moves into production, the name of the game is in building a system that is able to **regularly** ship **improved** models with **minimal effort**. The better you get at this, the more models you can build!
>
> - Running through the model pipeline on a regular cadence and focusing on shipping models that are better than before. Get a new and improved model into production every week or less!
> - Setting up a good feedback loop from the model outputs back to the development process. Figure out what examples the model does poorly on and add more examples to your training dataset.
> - Automating tasks in the pipeline that are particularly burdensome and building a team structure that allows your team members to focus on their areas of expertise. Tesla’s Andrej Karpathy calls the ideal end state “[Operation Vacation](https://www.braincreators.com/brainpower/insights/teslas-data-engine-and-what-we-should-all-learn-from-it).” I say, set up a workflow where you can send your ML engineers to the gym and let your ML pipeline do the heavy lifting!

> ## Always Be Iterating
>
> I used to think that machine learning was about the models. Actually, machine learning in production is about pipelines. One of the best predictors of success is the ability to effectively iterate on your model pipeline. That doesn't just mean iterating quickly, but also iterating intelligently. The second part is crucial, otherwise you end up with a pipeline that produces bad models very quickly.
>
> Unlike normal software development, the quality of an ML model depends on its implementation in code **and** on the data that code trains on. This dependency on the data means that the ML model can "explore" the input domain through dataset construction / curation, allowing it to understand the requirements of the task and adapt to it over time without necessarily having to modify the code.
>
> To take advantage of this property, machine learning needs a concept of continuous learning that emphasizes iteration on the data as well as the code. Machine learning teams have to:
>
> - Uncover problems in the data or model performance
> - Diagnose why the problems are happening
> - Change the data or the model code to solve these problems
> - Validate that the model is getting better after retraining
> - Deploy the new model and repeat
>
> Teams should try to go through this cycle at least every month. If you're good, maybe every week.
>
> ## Set Up A Feedback Loop
>
> **Set up a workflow where a human can review the outputs of your model and flag when an error occurs.** This is particularly appropriate when it’s easy for human review to catch mistakes across a lot of model inferences. The most common way this occurs is when customers notice mistakes in the model outputs and complain to the ML team. This is not to be underestimated, as this channel lets you directly incorporate customer feedback into the development cycle! A team can have humans double-check model outputs that a customer might miss: think of an operations person watching a robot sort packages on a conveyor belt and clicking a button whenever they notice an error occurring.
>
> **When the models run at too high a frequency for humans to check, consider setting up automated double-checking.** This is particularly useful when it’s easy to write “sanity checks” against the model outputs. For example, flagging whenever a lidar object detector and 2D image object detector disagree on a certain object, or when a frame-to-frame detector disagrees with a temporal tracking system. When it works, it provides a lot of helpful feedback on where failure cases occur. When it doesn’t work, it simply exposes errors in your checking system or misses out on situations where all the systems made an error, which is pretty low risk high reward.
>
> **Lastly, one can utilize feedback from the model’s feedback on the training set.** For example, examining the model’s disagreement with its training / validation dataset (i.e. high loss examples) surfaces high-confidence failures or labeling errors. Analysis of neural network embeddings can provide a way to understand patterns of failure modes in the training / validation dataset and find differences in the distribution of the raw data between the training and production datasets.
>
> ## Automate and Delegate
>
> A big part of iterating faster is reducing the amount of effort needed to do a single cycle of iteration. However, there’s always ways to make things easier, so one must prioritize what to improve. I like to think about effort in two ways: clock time and human time.
>
> In a production context, human time is a far more limited resource. Intermittent usage of human time also imposes significant switching costs and is inconvenient for the user. Generally, it’s much more important to automate away human time, especially when the time required comes from a skilled ML engineer. For example, it’s extremely common but wasteful to have multiple scripts that must be manually run in sequence with some manual moving of files between steps.
>
> Either way, it is important to minimize the amount of time (and associated costs) needed from humans to improve the model. While teams that are early on in the process might rely on an ML engineer to curate the dataset, it’s often more economical (or in the radiologist case, necessary) to have an operations user or domain expert without ML knowledge take on the heavy lifting of data curation. At that point, it becomes important to set up an operational process with good software tooling to label, quality check, improve, and version control the dataset.
>
> 
