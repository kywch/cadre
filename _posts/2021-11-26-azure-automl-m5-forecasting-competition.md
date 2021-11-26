---
layout: post
title: "Automated machine learning on the M5 forecasting competition"
author: Eric Wright
date: 2021-11-10
categories: ml/ai/nlp
tags: [mlops, azure]
---
[https://techcommunity.microsoft.com/t5/azure-ai-blog/automated-machine-learning-on-the-m5-forecasting-competition/ba-p/2933391](https://techcommunity.microsoft.com/t5/azure-ai-blog/automated-machine-learning-on-the-m5-forecasting-competition/ba-p/2933391)

> We announce here that Microsoft's [Automated Machine Learning](https://docs.microsoft.com/en-us/azure/machine-learning/concept-automated-ml), with nearly default settings, achieves a score in the 99th percentile of private leaderboard entries for the high-profile [M5 forecasting competition](https://www.kaggle.com/c/m5-forecasting-accuracy). Customers use Automated Machine Learning (AutoML) for ML applications in regression, classification, and time series forecasting. For example, [The Kantar Group](https://customers.microsoft.com/en-us/story/1433148684219960130-kantar-group-media-entertainment-azure-machine-learning) leverages AutoML for churn analysis, allowing clients to boost customer loyalty and increase their revenue.
>
> Our M5 result demonstrates the power and effectiveness of our [Many Models Solution](https://aka.ms/manymodelssolutions) which combines classical time-series algorithms and modern machine learning methods. Many Models is used in production pipelines by customers such as [AGL](https://customers.microsoft.com/en-gb/story/844796-agl-energy-azure), [Adamed](https://customers.microsoft.com/en-gb/story/815673-adamed-group-pharmaceuticals-power-bi), and [Oriflame](https://customers.microsoft.com/en-gb/story/1356512351216544667-oriflame-retailers-azure-en-czech-republic) for demand forecasting applications. We also use our [open-source Responsible AI tools](https://github.com/interpretml/interpret-community) to understand how the model leverages information in the training data. All computations take place on our scalable, cloud-based [Azure Machine Learning](https://azure.microsoft.com/en-us/services/machine-learning/) platform.

> ## [The M5 Competition](https://www.kaggle.com/c/m5-forecasting-accuracy)
>
> The M5 Competition, the fifth iteration of the Makridakis time-series forecasting competition, provides a useful benchmark for retail forecasting methods. The data contains historical daily sales information for about 3,000 products from 10 different Wal-Mart retail store locations. As is often the case in retail scenarios, the data has hierarchical structure along product catalog and geographic dimensions. Data features like sales price, SNAP (food stamp) eligibility, and calendar events are provided by the organizers in addition to historical sales. The accuracy track of the competition evaluates 28-day-ahead forecasts for 30,490 store-product combinations. With submissions from over 5,000 teams and 24 baseline models, the competition provides a rich set of comparisons between different modeling strategies.

> ## Feature Importance
>
> Most of AutoML's models can make use of the data features beyond the historical sales, so we find yet more insight into the composite model by examining the impact, or importance, of these features relative to the model's average prediction. A common way to quantify feature importance is with game-theoretic [Shapley value estimates](https://github.com/slundberg/shap). AutoML optionally calculates these for the best model selected from sweeping, so we make use of them here by aggregating values over all models in the composite.
>
> In the feature importance chart, we distinguish between features present in the original dataset, such as price, and those engineered by AutoML to aid model accuracy. Evidently, engineered features associated with the calendar and a seasonal decomposition make the most impact on predictions. The seasonal decomposition is derived from weekly sales patterns detected by AutoML. Price is the most important of the original features which is expected in retail scenarios given the likely significant effects of price on demand.

