---
layout: post
title: "The Batch: Special issue! Foundational algorithms, where they came from, where they're going"
author: Andrew Ng
date: 2022-05-25
categories: ml/ai/nlp
tags: recsys
---

[https://info.deeplearning.ai/the-batch-special-issue-foundational-algorithms-where-they-came-from-where-theyre-going](https://info.deeplearning.ai/the-batch-special-issue-foundational-algorithms-where-they-came-from-where-theyre-going)

> *In that spirit, this week’s issue of* The Batch *explores some of our field’s most important algorithms, explaining how they work and describing some of their surprising origins. If you’re just starting out, I hope it will demystify some of the approaches at the heart of machine learning. For those who are more advanced, you’ll find lesser-known perspectives on familiar territory.* 
>
> ## Linear Regression: Straight & Narrow 
>
> Linear regression may be the key statistical method in machine learning, but it didn’t get to be that way without a fight. Two eminent mathematicians claimed credit for it, and 200 years later the matter remains unresolved. The longstanding dispute attests not only to the algorithm’s extraordinary utility but also to its essential simplicity.
>
> **Coping with ambiguity:** Of course, data is never perfectly measured, and some variables are more important than others. These facts of life have spurred more sophisticated variants. For instance, linear regression with regularization (also called [ridge regression](https://en.wikipedia.org/wiki/Tikhonov_regularization?utm_campaign=The Batch&utm_source=hs_email&utm_medium=email&_hsenc=p2ANqtz-95w39cDuMjlkr9xxtGNh9-QfvymwP4L5WHTcP9224H-SCc-zBY4INssBopl9cBpwPYAD1x)) encourages a linear regression model to not depend too much on any one variable, or rather to rely evenly on the most important variables. If you’re going for simplicity, a different form of regularization (L1 instead of L2) results in [lasso](https://en.wikipedia.org/wiki/Lasso_(statistics)?utm_campaign=The Batch&utm_source=hs_email&utm_medium=email&_hsenc=p2ANqtz-95w39cDuMjlkr9xxtGNh9-QfvymwP4L5WHTcP9224H-SCc-zBY4INssBopl9cBpwPYAD1x), which encourages as many coefficients as possible to be zero. In other words, it learns to select variables with high prediction power and ignores the rest. [Elastic net ](https://en.wikipedia.org/wiki/Elastic_net_regularization?utm_campaign=The Batch&utm_source=hs_email&utm_medium=email&_hsenc=p2ANqtz-95w39cDuMjlkr9xxtGNh9-QfvymwP4L5WHTcP9224H-SCc-zBY4INssBopl9cBpwPYAD1x)combines both types of regularization. It’s useful when data is sparse or features appear to be correlated.
>
> ## Logistic Regression: Follow the Curve
>
> There was a moment when logistic regression was used to classify just one thing: If you drink a vial of poison, are you likely to be labeled “living” or “deceased”? Times have changed, and today not only does calling emergency services provide a better answer to that question, but logistic regression is at the very heart of deep learning.
>
> **More outcomes:** Verhulst’s work found the probabilities of binary outcomes, ignoring further possibilities like which side of the afterlife a poison victim might land in. His successors extended the algorithm:
>
> - Working independently in the late 1960s, British statistician [David Cox](https://scholar.google.com/scholar_lookup?hl=en&publication_year=1966&pages=55-71&author=D. R. Coxauthor%3DF. N. David&title=Some procedures associated with the logistic qualitative response curve&utm_campaign=The Batch&utm_source=hs_email&utm_medium=email&_hsenc=p2ANqtz-95w39cDuMjlkr9xxtGNh9-QfvymwP4L5WHTcP9224H-SCc-zBY4INssBopl9cBpwPYAD1x) and Dutch statistician [Henri Theil](https://www.jstor.org/stable/2525642?casa_token=PyEOSgvoa4cAAAAA%3A4t757YdDeEwOHZlGH06W7GOd5djaJjP1_eRkv5V8UqPhL1sKTwzsw6FmD6veSI_hL9X3CbPdhaTcKbEj8I0aoDwHQ46Vv34C2EXgKrXMvmXrXwy7NA&seq=1&utm_campaign=The Batch&utm_source=hs_email&utm_medium=email&_hsenc=p2ANqtz-95w39cDuMjlkr9xxtGNh9-QfvymwP4L5WHTcP9224H-SCc-zBY4INssBopl9cBpwPYAD1x) adapted logistic regression for situations that have more than two possible outcomes. 
> - Further work yielded [ordered logistic regression](https://www.jstor.org/stable/2984952?utm_campaign=The Batch&utm_source=hs_email&utm_medium=email&_hsenc=p2ANqtz-95w39cDuMjlkr9xxtGNh9-QfvymwP4L5WHTcP9224H-SCc-zBY4INssBopl9cBpwPYAD1x), in which the outcomes are ordered values.
> - To deal with sparse or high-dimensional data, logistic regression can take advantage of the same regularization techniques as linear regression. 
>
> **Versatile curve:** The logistic function describes a wide range of phenomena with fair accuracy, so logistic regression provides serviceable baseline predictions in many situations. In medicine, it estimates mortality and risk of disease. In political science, it predicts winners and losers of elections. In economics, it forecasts business prospects. More important, it drives a portion of the neurons, in which the nonlinearity is a sigmoid, in a wide variety of neural networks. 
>
> ## Gradient Descent: It’s All Downhill
>
> Imagine hiking in the mountains past dusk and finding that you can’t see much beyond your feet. And your phone’s battery died so you can’t use a GPS app to find your way home. You might find the quickest path down via gradient descent. Just be careful not to walk off a cliff. 
>
> **Stuck in the valley:** Too bad your phone is out of juice, because the algorithm may not have propelled you to the bottom of a convex mountain. You may be stuck in a nonconvex landscape of multiple valleys (local minima), peaks (local maxima), saddles (saddle points), and plateaus. ... For example, the algorithm may have [momentum ](https://distill.pub/2017/momentum/?utm_campaign=The Batch&utm_source=hs_email&utm_medium=email&_hsenc=p2ANqtz-95w39cDuMjlkr9xxtGNh9-QfvymwP4L5WHTcP9224H-SCc-zBY4INssBopl9cBpwPYAD1x)that helps it zoom over small rises and dips, giving it a better chance at arriving at the bottom. Researchers have devised so many variants that it may seem as though there are as many optimizers as there are local minima. Luckily, local and global minima tend to be [roughly equivalent](https://arxiv.org/abs/1412.0233?utm_campaign=The Batch&utm_source=hs_email&utm_medium=email&_hsenc=p2ANqtz-95w39cDuMjlkr9xxtGNh9-QfvymwP4L5WHTcP9224H-SCc-zBY4INssBopl9cBpwPYAD1x).
>
> **Optimal optimizer:** Gradient descent is the clear choice for finding the minimum of any function. In cases where an exact solution can be computed directly — say, a linear regression task with lots of variables — it can approximate one, often faster and more cheaply. But it really comes into its own in complex, nonlinear tasks. Armed with gradient descent and an adventurous spirit, you might just make it out of the mountains in time for dinner.
>
> ## Neural Networks: Find the Function
>
> Let’s get this out of the way: A brain is not a cluster of graphics processing units, and if it were, it would run software far more complex than the typical artificial neural network. Yet neural networks were inspired by the brain’s architecture: layers of interconnected neurons, each of which computes its own output depending on the states of its neighbors. The resulting cascade of activity forms an idea — or recognizes a picture of a cat.
>
> **Black box:** While a trained network may perform its task, good luck determining how. You can read the final function, but often it’s so complex — with thousands of variables and nested activation functions — that it’s exceedingly difficult to explain how the network succeeded at its task. Moreover, a trained network is only as good as the data it learned from. For instance, if the dataset was skewed, the network’s output will be skewed. If it included only high-resolution pictures of male cats, there’s no telling how it would respond to lower-resolution images.
>
> ## Decision Trees: From Root to Leaves
>
> What kind of beast was Aristotle? The philosopher's follower Porphyry, who lived in Syria during the third century, came up with a logical way to answer the question. He organized Aristotle’s proposed “categories of being” from general to specific and assigned Aristotle himself to each category in turn: Aristotle’s substance occupied space rather than being conceptual or spiritual; his body was animate not inanimate; his mind was rational not irrational. Thus his classification was human. Medieval teachers of logic drew the sequence as a vertical flowchart: An early decision tree.
>
> **Raking leaves:** Decision trees do have some drawbacks. They can easily overfit the data by growing so many levels that leaf nodes include as few as one example. Worse, they’re prone to the butterfly effect: Change one example, and the tree that grows could look dramatically different. 
>
> **Into the woods:** Turning this trait into an advantage, American statistician Leo Breiman and New Zealander statistician Adele Cutler in 2001 developed the [random forest](https://link.springer.com/article/10.1023/A:1010933404324?utm_campaign=The Batch&utm_source=hs_email&utm_medium=email&_hsenc=p2ANqtz-95w39cDuMjlkr9xxtGNh9-QfvymwP4L5WHTcP9224H-SCc-zBY4INssBopl9cBpwPYAD1x), an ensemble of decision trees, each of which processes a different, overlapping selection of examples that vote on a final decision. Random forest and its cousin XGBoost are less prone to overfitting, which helps make them among the most popular machine learning algorithms. It’s like having Aristotle, Porphyry, Blumenbach, Darwin, Jane Goodall, Dian Fossey, and 1,000 other zoologists in the room together, all making sure your classifications are the best they can be.
>
> ## K-Means Clustering: Group Think
>
> If you’re standing close to others at a party, it’s likely that you have something in common. This is the idea behind using k-means clustering to split data points into groups. Whether the groups formed via human agency or some other force, this algorithm will find them. 
>
> **Power to the data points:** The idea has spawned a few notable variations:
>
> - [K-medoids](https://onlinelibrary.wiley.com/doi/abs/10.1002/9780470316801.ch2?utm_campaign=The Batch&utm_source=hs_email&utm_medium=email&_hsenc=p2ANqtz-95w39cDuMjlkr9xxtGNh9-QfvymwP4L5WHTcP9224H-SCc-zBY4INssBopl9cBpwPYAD1x) use actual data points as centroids rather than mean positions in a given cluster. The medoids are points that minimize the distance to all other points in their cluster. This variation is more interpretable because the centroids are always data points.
> - [Fuzzy C-Means Clustering](https://www.tandfonline.com/doi/abs/10.1080/01969727308546046?utm_campaign=The Batch&utm_source=hs_email&utm_medium=email&_hsenc=p2ANqtz-95w39cDuMjlkr9xxtGNh9-QfvymwP4L5WHTcP9224H-SCc-zBY4INssBopl9cBpwPYAD1x) enables the data points to participate in multiple clusters to varying degrees. It replaces hard cluster assignments with degrees of membership depending on distance from the centroids.
>
> **Revelry in \*n\* dimensions:** Nonetheless, the algorithm in its original form remains widely useful — especially because, as an unsupervised algorithm, it doesn’t require gathering potentially expensive labeled data. It’s also ever faster to use. For instance, machine learning libraries including scikit-learn benefit from the 2002 addition of [kd-trees](http://www.cs.umd.edu/~mount/Papers/pami02.pdf?utm_campaign=The Batch&utm_source=hs_email&utm_medium=email&_hsenc=p2ANqtz-95w39cDuMjlkr9xxtGNh9-QfvymwP4L5WHTcP9224H-SCc-zBY4INssBopl9cBpwPYAD1x) that partition high-dimensional data extremely quickly. 
