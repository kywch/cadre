---
layout: post
title: "PEER: A collaborative language model"
author: Timo Schick, Jane Dwivedi-Yu, Zhengbao Jiang, et al.
date: 2022-08-24
categories: ml/ai/nlp
tags: large-language-model
---

[https://ar5iv.labs.arxiv.org/html/2208.11663](https://ar5iv.labs.arxiv.org/html/2208.11663)

> Text from current language models can be useful as a rough draft, but that leaves the polishing to human writers. A language model learned how to generate and respond to editorial directions. What’s new: Timo Schick and colleagues at Meta proposed Plan, Edit, Explain, and Repeat (PEER), a text generator designed to collaborate with human writers.

> Key insight: Data that demonstrates the motivations, execution, and results of editing is hard to come by. **Wikipedia, in which every article includes a history of edits as well as comments on them, comes close,** but an editor trained solely on Wikipedia would be limited to encyclopedia-style text. However, a model trained on Wikipedia to undo revisions can synthesize a supplemental dataset of unrevised and revised examples. Applying the undo function to varied text can generate synthetic “unedited” drafts for training the editor.

> How it works: PEER comprises four T5 large language models: PEER-Edit (which executed revisions), PEER-Undo (which undid revisions), PEER-Explain (which explained revisions), and PEER-Document (which generated synthetic primary-source documents as a basis for revisions). The authors trained them on **Wikipedia, 6.9 million examples that include texts before and after a revision, a revision plan** (a directive to revise the text, such as “add information about the scandal”), **an explanation (a reason for the revision, which may duplicate the revision plan)**, and cited documents (primary sources on which the text is based).

> Why it matters: Training text generators to provide explanations for their decisions and citations for the facts they use may lead to more interpretable models.

> We’re thinking: The raw output of generative models is fun and exciting, but imagine their potential as collaborators with creative people!