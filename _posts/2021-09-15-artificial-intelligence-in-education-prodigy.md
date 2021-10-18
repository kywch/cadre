---
layout: post
title: "Artificial Intelligence in Education (from Prodigy)"
author: Aaron Wang
date: 2021-09-15
categories: [ml/ai/nlp, education]
tags: prodigy
---
[https://medium.com/prodigy-engineering/artificial-intelligence-in-education-8e9309aac08b](https://medium.com/prodigy-engineering/artificial-intelligence-in-education-8e9309aac08b)

> **AI Algorithms in Education**
> 
> There are many AI algorithms we can leverage to bring the aforementioned benefits. The algorithms here are a broader category of machine learning. Some of them will not require machine learning at all but using their machine learning or deep learning alternatives can increase the accuracy.

> **Education Equity: Optical character recognition (OCR)** is the electronic or mechanical conversion of images of typed, handwritten, or printed text into machine-encoded text. OCR can improve education equity by establishing an async connection between remote teachers and students as an alternative way of getting inputs from students who may lack consistent access to devices with an internet connection. OCR also provides the foundation for natural language processing by digitalizing handwriting data onto the cloud, which educators can analyze afterward.

> **Education Efficiency: Natural language processing (NLP)** is concerned with the interactions between computers and human language, and in particular, how to program computers to process and analyze large amounts of natural language data. According to a study titled [Natural Language Processing for Enhancing Teaching and Learning](https://ojs.aaai.org/index.php/AAAI/article/view/9879), NLP improves education efficiency by liberating teachers from repetitive tasks and offering schools analytical reports on student performance. NLP can offer automatic language assessment (summative), intelligent tutoring (formative), dialogue generation, chat room regulation, material recommendation, and question generation.

> **Education Quality: Recommender System** seeks to predict the “rating” or “preference” a user would give to an item. Recommender system improves education quality by leveraging teacher-generated data to offer personalized content to students. It can recommend or auto-allocate assignments, plans, and test preps to teachers. It can also recommend additional learning resources to parents.

> **Enablers: Procedural content generation (PCG)** is the process of creating data algorithmically rather than manually to create textures and 3D models in computer graphics and a large amount of content in games.

> **AI at Prodigy: A Case Study on Math Tutoring**
> 
> Prodigy has been leveraging machine learning for a while to automate some tasks. [Prodigy Math Tutoring](https://www.prodigygame.com/main-en/tutoring/), for example, is an important part of our business model that complements the math game by providing customized tutoring to suit each student’s personal learning pace and needs.
> 
> We get a large number of requests for [free sessions](https://www.prodigygame.com/tutoring/public/identification/) on a daily basis. And guess what, a lot of the requests are from students who think they will get free in-game items through bookings, which is not actually the case. Here are some real booking messages we got from students.
>
> - La-la, la-la, la-la
> - let him be a member pls
> - i do math and have fun
> 
> While some students’ responses are humorous, it did pose a challenge for us as it took time to filter out the real parents and guardians.
>
> And that’s where machine learning comes into play. We manually cleaned up thousands of booking requests and tagged them as either legitimate or not. Then we fed the data to a [Naive Bayes classifier](https://en.wikipedia.org/wiki/Naive_Bayes_classifier) which tokenizes the individual words and predicts the result based on the Bayes Theorem.