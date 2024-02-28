# Uber---Bloc-3
Predictive analysis of structured data by artificial intelligence.


my email: anastasia@phiskills.com

video-explanation: https://youtu.be/oDzZkGvfSyY

## Goal

In this project the goal was to create algorithms that will determine where are the hot-zones that drivers should be in.

## Preprocessing

As we have a lot of files with data I thought that the best way will be to create an algorithm that consists of functions. So that is how with the first function can choose any month that we need.

Next we can start analysing and transform our dataset the way we need it.
As we have a column “Base”, I thought that the number of bases we can use to define the number of clusters. So that is how we can plan how bases should be located for the future to make Uber be more efficient.

Next we see column “Date/Time” that needs to be spliced in two “Date” and “Time”. That is how we can also do split on the column “Time”to create new columns “Hour”,”Minutes”, “Seconds”.

Our data contains information on the dates, but it's not very easy information to do clusters on, as these dates really don't give us a lot. By we can categorize them into days of the week. We can also simplify our code if we categorize hours too into day time.

It is very possible that our dataset contains a lot of data, so we need to check if it would be better to take a sample of a smaller amount of observations.

Getting day of the week and day time

After doing all the preprocessing, I created a function that can easily create a new data frame with already filtered day of the week and day time that we need. For example, it will be …

After that we can go to the clustering part.

## Clustering

Here I tried to do KMeans and DBSCAN clustering.

Basically, I created functions that just do everything. Number of clusters equals the number of bases (that we specified at the very beginning) , random state 42, just so every time it will be exactly the same result. And a StandardScaler to standardise our new dataset, on which we make clustering.

So, here we get our results for (day, time)….
With DBSCAN I tried to use epsilon 0,2 and the minimum number of points to form a dense region 100. 

So as we see he created 5 clusters too, but they are not that great to compare to the KMeans clusters. 
