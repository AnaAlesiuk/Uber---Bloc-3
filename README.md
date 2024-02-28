# Uber---Bloc-3
Predictive analysis of structured data by artificial intelligence.


my email: anastasia@phiskills.com

video-explanation: https://youtu.be/oDzZkGvfSyY

## Goal

In this project, the goal was to create algorithms that would determine where are the hot zones that drivers should be in.

## Preprocessing

As we have a lot of files with data, I thought that the best way would be to create an algorithm that consists of functions. So that is how, with the first function, we can choose any month that we need.

Next, we can start analyzing and transforming our dataset the way we need it.
As we have a column “Base” I thought we can use the number of bases to define the number of clusters. So that is how we can plan how bases should be located for the future to make Uber be more efficient.

Next, we see the column “Date/Time” that needs to be spliced in two: “Date” and “Time”. That is how we can also do split on the column “Time” to create new columns “Hour”,” Minutes”, “Seconds”.

Our data contains information on the dates, but it's not very easy information to do clusters on, as these dates really don't give us a lot. By we can categorize them into days of the week. We can also simplify our code if we categorize hours into daytime.

Our dataset may contain a lot of data, so we need to check if it would be better to take a sample of a smaller amount of observations.

## Getting the day of the week and daytime

After doing all the preprocessing, I created a function that can easily create a new data frame with the already filtered day of the week and daytime that we need. For example, it will be …

After that, we can go to the clustering part.

## Clustering

Here, I tried to do KMeans and DBSCAN clustering.

I created functions that just do everything. The number of clusters equals the number of bases (that we specified at the very beginning), random state 42, just so every time it will be exactly the same result. And a StandardScaler to standardize our new dataset, on which we make clustering.

So, here we get our results for (day, time)….
With DBSCAN I tried to use epsilon 0,2 and the minimum number of points to form a dense region 100. 

So, as we see, he created 5 clusters, too, but they are not that great to compare to the KMeans clusters. 
