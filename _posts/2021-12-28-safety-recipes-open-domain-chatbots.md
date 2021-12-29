---
layout: post
title: "Recipes for safety in open-domain chatbots"
author: Jing Xu, Emily Dinan, et al.
date: 2021-08-04
categories: [research, ml/ai/nlp]
tags: chatbot
---

[https://arxiv.org/pdf/2010.07079.pdf](https://arxiv.org/pdf/2010.07079.pdf)

[https://parl.ai/projects/safety_recipes/](https://parl.ai/projects/safety_recipes/)

[https://parl.ai/](https://parl.ai/), [https://github.com/facebookresearch/ParlAI](https://github.com/facebookresearch/ParlAI)

> Models trained on large unlabeled corpora of human interactions will learn patterns and mimic behaviors therein, which include offensive or otherwise toxic behavior and unwanted biases. 
>
> We investigate a variety of methods to mitigate these issues in the context of open-domain generative dialogue models. 
>
> We introduce a new human-and-model-in-the-loop framework for both training safer models and for evaluating them, as well as a novel method to distill safety considerations inside generative models without the use of an external classifier at deployment time. 
>
> We conduct experiments comparing these methods and find our new techniques are (i) safer than existing models as measured by automatic and human evaluations while (ii) maintaining usability metrics such as engagingness relative to the state of the art. 
>
> We then discuss the limitations of this work by analyzing failure cases of our models.

> In a detailed comparison study, we find that two new techniques we propose are promising avenues of research: (i) baking-in safety into generative models, and (ii) building adversarial human-bot conversation robustness into two-stage models. We find that both of these techniques outperform their respective generative or two-stage model counterparts. To aid this study we have investigation techniques of crowdsourcing safety evaluations, and built an adversarially created dialogue safety training and evaluation set, which we will publicly release, along with our models in ParlAI. 
