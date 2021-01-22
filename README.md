# Fantasy-Football-Help

This GitHub page will provide code for fantasy football statistics such as a variable's effect on their PPR.

# Table of Contents

* [NFL Cluster Analysis](https://github.com/mattflaherty97/Fantasy-Football-Help/tree/main/cluster_analysis)
* [Titans Fake Punt](https://github.com/mattflaherty97/Fantasy-Football-Help/tree/main/titans_fake_punt)

# Cluster Analysis of RBs

## Data

The data used for this data set is collected from [Pro Football Reference](https://www.pro-football-reference.com/). I use RB data from [2019](https://www.pro-football-reference.com/years/2019/fantasy.htm) and [2020](https://www.pro-football-reference.com/years/2020/fantasy.htm) to gather fantasy football statistics because my goal is to use these statistics to find the best players for a fantasy football team. I also join in advanced rushing statistics from [2019](https://www.pro-football-reference.com/years/2019/rushing_advanced.htm) and [2020](https://www.pro-football-reference.com/years/2020/rushing_advanced.htm) to do a deepers analysis in order to see which players would be best to have on a team. I also use this data to determine which features have the biggest impact on PPR (measure of performance for fantasy football players). As players get traded and new players enter the league, it is not always beneficial to use previous years statistics to determine how well a player will perform. Thus, finding important features will allow me to draft players that are predicted to perform well in these important features.

## Cluster analysis for RBs

In this [file](https://github.com/mattflaherty97/Fantasy-Football-Help/blob/main/cluster_analysis.md), I want to find RBs that are similar to each other. I use a k-means cluster with k equal to 3 so I have 3 different clusters of RBs that perform similarly in yards before contact, yards after contact, targets, and PPR. I chose a k value equal to 3 by using an elbow plot for clusters with the "total within sum of square" values. After 3 clusters, there is not a significant decrease in the value.

![Elbow Plot](https://github.com/mattflaherty97/Fantasy-Football-Help/blob/main/cluster_analysis/cluster_analysis_files/figure-gfm/unnamed-chunk-4-1.png)

This is the plot of player clusters that was developed by the cluster analysis. The graph itself is not very interpretable except for the second (green) cluster and a few in the first (red) cluster. Although the graph is not interpretable, the process of developing clusters for the RBs allowed me to put the player's cluster number in their observation in the data frame. Having done this, I can filter the data frame by cluster number to see which players fit into each cluster. This could be beneficial on draft night because I might want to make sure all RBs from cluster 2 (green) are chosen before moving to cluster 1 (red).

![Cluster Analysis](https://github.com/mattflaherty97/Fantasy-Football-Help/blob/main/cluster_analysis/cluster_analysis_files/figure-gfm/unnamed-chunk-5-1.png)

# [Titans Fake Punt](https://github.com/mattflaherty97/Fantasy-Football-Help/blob/main/titans_fake_punt/titans_tracking.ipynb)

January 7, 2021 marked the final day for [Big Data Bowl](https://www.kaggle.com/c/nfl-big-data-bowl-2021) submissions. Big Data Bowl is a competition open to any one interested in using NFL player tracking data. I want not able to get a submission in on time; however, I took the advantage of having open notebooks to make my own visualization. This notebook is an animation of the Tennessee Titans longest passing play in the 2018 season. This is my first animation and I hope to not only make more of these visualizations but make visualizations that can be analyzed for future use.

## Data

Data for the Big Data Bowl can be found [here](https://www.kaggle.com/c/nfl-big-data-bowl-2021/data). As the data is player tracking data, it is quite large and cannot be uploaded to GitHub because of size restrictions.

Player tracked play:

![Player Track](https://github.com/mattflaherty97/Fantasy-Football-Help/blob/main/titans_fake_punt/titans_fk_punt.gif)

Here is the actual play:

![Actual Play](https://github.com/mattflaherty97/Fantasy-Football-Help/blob/main/titans_fake_punt/gif.gif)
