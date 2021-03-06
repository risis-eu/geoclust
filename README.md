# GeoClust
GeoClust is a simple solution to study the geographical aggregation of activities. This is done by grouping coordinates (latitude and longitude) into clusters. This has been developed by members of the [platform CorText](http://www.cortext.net/) for the [RISIS project](http://risis.eu/).

##  The software is based on two different approaches
First we use a density-based algorithm, DBSCan (Ester, Kriegel, & Sander, 1996), to identify the area where the activities are concentrated. Following the original algorithm two parameters are fixed before the calculation: all points of a cluster are surrounded by at least X points in a circle with a diameter of Y km. We have added the ability to weighted each X points; the software examines the quantity of activities for each couple of coordinates. This step builds initial clusters.  
The second step builds the final clusters by using the CHAMELEON method (Karypis, Han, & Kumar, 1999). The software compares two different dimensions of the initial clusters (relational and structural analysis) to merge them if the thresholds are reached:

1. RI or Relative Interconnectivity: how intense are the relations between the initial clusters (with less than 100 km between the centroids)? 
2.	RC or Relative Closeness: does the final cluster will have a similar profile of collaborations than the two initial clusters taken separately (to avoid large variations of density of links in the final cluster)? 

##  How to use
Import the project into Eclipse, and add the jar libraries found into the folder external-libs

##  More information on the algorithms
Ester, M., Kriegel, H.-P., & Sander, J. (1996). *A density-based algorithm for discovering clusters in large spatial databases with noise.* In S. Evangelos, J. Han, & U. M. Fayyad (Eds.), 2nd International Conference on Knowledge Discovery and Data Mining (KDD-96) (pp. 226–231). AAAI Press.  
Karypis, G., Han, E.-H., & Kumar, V. (1999). *Chameleon: Hierarchical clustering using dynamic modeling.* IEEE Computer, 32(8), 68–75.

##  Licence
MIT License (MIT), Copyright (c) 2015 CorText  
Lionel Villard, ESIEE Paris, CorText Platform, Paris Est University  
Michel Revollo, ESIEE Paris, Paris Est University
