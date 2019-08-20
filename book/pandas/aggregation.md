---
layout: default
---


![](https://cdn-images-1.medium.com/max/1200/1*QI2iTWNPA1ZU-yRtCKm1Pw.jpeg)

Aggregation is the **_process of converting a list or series of values into a single value_**.

First, let’s load some data for our demo. This is movie data will contain only 2 columns, `movie_title` and `duration`.

![](https://cdn-images-1.medium.com/max/800/1*AFl_GiOAHaSwGMt-7cnAWQ.png)

Let’s go through function by function with the demo data..

### How many movies exist in the data set

To answer this, we use function called `count()`. This function simply returns the number of values inside the series. So we have exactly 5043 movies in this data set.

![](https://cdn-images-1.medium.com/max/800/1*hYZpA2CSd57opU9SdIZKzA.png)

### Calculate total duration for all movies

To solve this, we use the function `sum()`. This function returns the sum of all values in a series.

![](https://cdn-images-1.medium.com/max/800/1*5wEFZTIklbzgCxauYf2mIA.png)

### Printout shortest, longest, and mean of duration

Easy to know that we will use `min()`, `max()`, and `mean()` function

![](https://cdn-images-1.medium.com/max/800/1*UXl03YhbTBnMxlnKqcXP5w.png)

### That’s it

We now know the basic aggregation functions of Python.
