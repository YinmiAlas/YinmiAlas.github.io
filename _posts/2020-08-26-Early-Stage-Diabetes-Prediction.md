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


This graphs visually shows us how strong a player is across all his player attributes.


![attribute2](/assets/img/thirdpic.jpg)



# The Best 10 Players Value against Release Clause.

What does paying a release clause mean?

A manager can sign a player by paying his release clause, which will be higher than the market value of the player, without having to depend on the owner of the player.



<iframe width="900" height="800" frameborder="0" scrolling="no" src="//plotly.com/~YinmiAlas/3.embed"></iframe>




## How are release clauses set?

Initially, a player’s release clause is established automatically according to the following rules:

* Players with a Market Value < 1M will have a release clause of 1M.
* Players with a Market Value > 1M will have a release clause of 166% of their market value.

The release clause can never be less than the market value. As such, it will be updated in keeping with the market value. Any user who wants to protect their players can raise the release clause by paying from their budget to a ratio of 1:2. For example, if you want to raise the release clause by 2M, you will have to pay 1M from your budget.



# Average Age of the first 100 Players.
According to the data set of the first 100 FIFA players the average age is 27.



<iframe width="900" height="800" frameborder="0" scrolling="no" src="//plotly.com/~YinmiAlas/6.embed"></iframe>





# The Preferred Foot and Weak Foot of the first 100 players.
we can clearly see that the majority of the players in the game are gifted for their profession, as well as the famous echoes and the best in their environment.



<iframe width="900" height="800" frameborder="0" scrolling="no" src="//plotly.com/~YinmiAlas/8.embed"></iframe>




Mean while down here we have the weak foot of the first 100 players who are rated from 1 to 5, each one has their own level of support with respect to their preferred foot, some players their weak foot does not help them at all and others their weak foot is handled perfectly.




<iframe width="900" height="800" frameborder="0" scrolling="no" src="//plotly.com/~YinmiAlas/10.embed"></iframe>





# Which Country has the most players in FIFA 19.

From the entire dataset we get the 5 most common nationalities in FIFA 19. As you can see England is the most frequent nationality with 1,662 records, followed by Germany with 1,198 and Spain with 1,072.




<iframe width="900" height="800" frameborder="0" scrolling="no" src="//plotly.com/~YinmiAlas/12.embed"></iframe>





# Which features of the first 100 players are highly correlated.

We will generate a heat map from the numerical columns which will show us how strongly correlated each variable is with the other. We filtered the dataframe so that it only includes numerical values and generate a heat map from the resulting dataframe:



<iframe width="900" height="800" frameborder="0" scrolling="no" src="//plotly.com/~YinmiAlas/14.embed"></iframe>





# The best 10 players Potential against Wage

You can clearly see how some players have less potential than others and earn more and others that their potential is almost at their maximum and earn what they deserve. I made this graph to see if the players earn what they deserve for their high potential.



<iframe width="900" height="800" frameborder="0" scrolling="no" src="//plotly.com/~YinmiAlas/16.embed"></iframe>







There is much more to analyze but I will stop here. The code of this post will be available on [Github](LS_DS__build_week_project.ipynb). Thank you for reading!

