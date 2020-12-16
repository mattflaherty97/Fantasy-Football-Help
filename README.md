# Fantasy-Football-Help

This GitHub page will provide code for fantasy football statistics such as a variable's effect on their PPR.

# Statistics that affect PPR
[PPR vs RB stats]

# Cluster analysis for RBs

In this file I want to find RBs that are similar to each other. I use a k-means cluster with k equal to 3 so I have 3 different clusters of RBs that perform similarly in yards before contact, yards after contact, targets, and PPR. I chose a k value equal to 3 by using an elbow plot for clusters with the "total within sum of square" values. After 3 clusters, there is not a significant decrease in the value.

![Elbow Plot](https://github.com/mattflaherty97/Fantasy-Football-Help/blob/main/cluster_analysis_files/figure-gfm/unnamed-chunk-4-1.png)

This is the plot of player clusters that was developed by the cluster analysis. The graph itself is not very interpretable except for the second (green) cluster and a few in the first (red) cluster. Although the graph is not interpretable, the process of developing clusters for the RBs allowed me to put the player's cluster number in their observation in the data frame. Having done this, I can filter the data frame by cluster number to see which players fit into each cluster. This could be beneficial on draft night because I might want to make sure all RBs from cluster 2 (green) are chosen before moving to cluster 1 (red).

![Cluster Analysis](https://github.com/mattflaherty97/Fantasy-Football-Help/blob/main/cluster_analysis_files/figure-gfm/unnamed-chunk-5-1.png)
