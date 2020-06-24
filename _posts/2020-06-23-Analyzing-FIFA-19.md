---
layout: post
title: Analyzing FIFA 19 Dataset 
subtitle: The Best 10 Players of FIFA 19
cover-img: assets/img/EASportsFifa19.jpg
---

In this post we will perform a data analysis of the FIFA 19 data set. The data set can be found on [Kaggle](https://www.kaggle.com/karangadiya/fifa19). FIFA( Fédération Internationale de Football Association) and FIFA 19 is part of the FIFA series of association football video games is the one of the most popular game in the world, EA said that lifetime sales of the soccer franchise [has passed 260 million copies since its first launch in 1993](https://venturebeat.com/2018/09/05/ea-sports-fifa-franchise-surpasses-260-million-copies-sold/).

We will analyze FIFA 19 players. The dataset has 89 columns but we will use around 25 columns grabbing the most important ones of the dataset. Using the following topics:


* The Best 10 Players with their abilities.
* The Best 10 Players Value against Release Clause.
* Analyze Avarage Age of the first 100 Players.
* Analyze the Preferred Foot and Weak Foot of the first 100 players.
* Analyze Which Country has the most players in FIFA19.
* Which features of the first 100 players are highly correlated.
* The best 10 players Potential against Wage.



#### Let’s get started!!




# The Best 10 Players with their abilities.

Each corner of the polygon is one of the players attributes. The further away from the center, the higher the attribute. **The shape is convex**. Convex means that the player is generally balanced over all the attributes.


![attribute](/assets/img/firstpic.jpg)


A well rounded player like Messi will show a high percentage of the polygon shaded in while a weak player will show little shaded area near the middle.


![attribute1](/assets/img/FullSizeRender_8.JPG)


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

