---
layout: post
title: Early Stage Diabetes Risk Prediction 
subtitle: Using Machine Learning
cover-img: assets/unit2 pic/DIABETES_INFO_stats.png
---

In this post we will predict and perform evaluation Metrics of the Early Stage Diabetes Risk Prediction dataset. The dataset can be found on [UCI Machine learning repository](https://archive.ics.uci.edu/ml/datasets/Early+stage+diabetes+risk+prediction+dataset.#). Diabetes is a chronic, metabolic disease characterized by elevated levels of blood glucose (or blood sugar), which leads over time to serious damage to the heart, blood vessels, eyes, kidneys and nerves.

About 422 million people worldwide have diabetes, the majority living in low-and middle-income countries, and 1.6 million deaths are directly attributed to diabetes each year. Both the number of cases and the prevalence of diabetes have been steadily increasing over the past few decades.

The dataset has 17 columns and 520 rows we will use the following classification models with their metrics score:

* Logistic Regression.
* Decision Tree.
* Random Forest Classifier.
* XGBoost Classifier.



#### Let’s get started!!




# Processing the data.

![attribute](/assets/unit2 pic/Screen Shot 2020-08-25 at 9.21.43 PM.png)


![attribute1](/assets/unit2 pic/Screen Shot 2020-08-25 at 9.26.44 PM.png)


I need to split the data twice easy way to get Train/Validate/Test random split.


![attribute2](/assets/unit2 pic/Screen Shot 2020-08-25 at 9.45.15 PM.png)



# Begin with baselines.

![attribute22](/assets/unit2 pic/Screen Shot 2020-08-25 at 9.12.19 PM.png)


“Class” is the feature we are going to predict, its has Positive and Negative values.

![attribute23](/assets/unit2 pic/Screen Shot 2020-08-25 at 9.13.03 PM.png)


![attribute24](/assets/unit2 pic/Screen Shot 2020-08-25 at 9.13.35 PM.png)


This is Baseline Accuracy score lets improve the score with a Classification Model.

![attribute25](/assets/unit2 pic/Screen Shot 2020-08-25 at 9.13.55 PM.png)

## Logistic Regression Model.

Logistic Regression is one of the most common classification algorithms.

![attribute26](/assets/unit2 pic/Screen Shot 2020-08-25 at 9.57.31 PM.png)

lets keep trying improving the score with more models
Validation Accuracy : 0.91%
Test ROC AUC : 0.98%

# Confusion Matrix Plot with Logistic Regression Model.

![attribute27](/assets/unit2 pic/Screen Shot 2020-08-26 at 5.19.00 PM.png)

This is what a confusion matrix looks like

![attribute28](/assets/unit2 pic/Screen Shot 2020-08-26 at 5.39.45 PM.png)

Now, let us understand what TP, TN, FP, FN denote in this matrix:

* **True Positives (TP):** These are cases in which we predicted yes (they have the disease), and they do have the disease.
* **True Negatives (TN):** We predicted no, and they don’t have the disease.
* **False Positives (FP):** We predicted yes, but they don’t actually have the disease. (Also known as a “Type I error.”)
* **False Negatives (FN):** We predicted no, but they actually do have the disease. (Also known as a “Type II error.”)

# Classification Report with Logistic Regression Model.

![attribute29](/assets/unit2 pic/Screen Shot 2020-08-26 at 5.45.16 PM.png)


Lets see how a Classification Report Works.

**Precision:** is defined as the number of true positives (TP) over the number of true positives plus the number of false positives (FP).

![attribute30](/assets/unit2 pic/imagen1.png)


**Recall:** is defined as the number of true positives (TP) over the number of true positives plus the number of false negatives (FN).

![attribute31](/assets/unit2 pic/image2.png)

**F1-score:** is the harmonic mean of precision and recall.

![attribute32](/assets/unit2 pic/imagen3.png)

# Permutation importances.

![attribute33](/assets/unit2 pic/Screen Shot 2020-08-26 at 5.59.31 PM.png)


![attribute34](/assets/unit2 pic/Screen Shot 2020-08-26 at 5.59.57 PM.png)


**The permutation feature importance:** is defined to be the decrease in a model score when a single feature value is randomly shuffled 1. This procedure breaks the relationship between the feature and the target, thus the drop in the model score is indicative of how much the model depends on the feature.




# Decision Tree Model.

![attribute35](/assets/unit2 pic/Screen Shot 2020-08-26 at 6.09.57 PM.png)



**Classification Accuracy Score:** is our starting point. It is the number of correct predictions made divided by the total number of predictions made, multiplied by 100 to turn it into a percentage.

In this model the Validation Accuracy Score increase: 0.06%

But Test ROC AUC Score decrease : 0.012




# Confusion Matrix Plot with Decision Tree Model.

![attribute36](/assets/unit2 pic/Screen Shot 2020-08-26 at 6.10.48 PM.png)


# Classification report with Decision Tree Model.

![attribute37](/assets/unit2 pic/Screen Shot 2020-08-26 at 6.11.08 PM.png)

# Visualizing the Desicion Tree Model.

![attribute38](/assets/unit2 pic/Screen Shot 2020-08-26 at 6.35.55 PM.png)


![attribute39](/assets/unit2 pic/Screen Shot 2020-08-26 at 6.35.33 PM.png)

# Visualizing The Feature Importances with Decision Tree Model.

![attribute40](/assets/unit2 pic/Screen Shot 2020-08-26 at 6.42.06 PM.png)


![attribute41](/assets/unit2 pic/Screen Shot 2020-08-26 at 6.42.59 PM.png)

# Random Forest Model

![attribute41](/assets/unit2 pic/Screen Shot 2020-08-26 at 6.44.45 PM.png)

**The AUC** is the area under the ROC curve. This score gives us a good idea of how well the model performances.
AUC ROC is one of the most important evaluation metrics for any classification model’s performance.

In this case the Accuracy score drop : 0.0087%
But the ROC AUC score is higher : 0.027%

# Confusion Matrix Plot with Random Forest Classifier.
![attribute42](/assets/unit2 pic/Screen Shot 2020-08-26 at 6.45.57 PM.png)

# Classification report with Random Forest Classifier.
![attribute43](/assets/unit2 pic/Screen Shot 2020-08-26 at 6.46.10 PM.png)

# Partial Dependence Plot, 1 feature isolation Using Random Forest Classifier

![attribute44](/assets/unit2 pic/Screen Shot 2020-08-26 at 7.06.04 PM.png)

![attribute45](/assets/unit2 pic/Screen Shot 2020-08-26 at 7.06.32 PM.png)

![attribute46](/assets/unit2 pic/Screen Shot 2020-08-26 at 7.06.50 PM.png)


**The partial dependence plot:** (short PDP plot) shows the marginal effect one or two features have on the predicted outcome of a machine learning model . A partial dependence plot can show whether the relationship between the target and a feature is linear, monotonic or more complex.


# Partial Dependence Plot, 2 features interaction Using Random Forest Classifier.

![attribute47](/assets/unit2 pic/SScreen Shot 2020-08-26 at 7.15.50 PM.png)

It would look like one gender has a much higher chance of diabetes than the other

![attribute48](/assets/unit2 pic/Screen Shot 2020-08-26 at 7.16.13 PM.png)

# XGBoost Classifier Model
## Shapley plot explaning multiples prediction using their index number or the row number using XgBoost

![attribute49](/assets/unit2 pic/Screen Shot 2020-08-26 at 7.18.16 PM.png)

![attribute50](/assets/unit2 pic/Screen Shot 2020-08-26 at 7.19.30 PM.png)

![attribute51](/assets/unit2 pic/Screen Shot 2020-08-26 at 7.20.03 PM.png)

The records for this plot are 103 patients and it looks like the prediction is negative with 0.43% and the probability to have diabetes is 0.57% .

![attribute52](/assets/unit2 pic/Screen Shot 2020-08-26 at 7.20.55 PM.png)

There is much more to analyze but I will stop here. The code of this post will be available on [Github](https://github.com/YinmiAlas/early-stage-diabetes-prediction). Thank you for reading!


