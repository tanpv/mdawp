---
layout: default
---

![](https://cdn-images-1.medium.com/max/2560/1*K1z-tfWyMk1CPRE_TO7tuw.jpeg)

Sorting is very important when working with a data table. This post will show you how sorting works in pandas.

First, let’s load some data. This data table is about movies from an IMDB data set. `imdb_score` is voted by people and means does this movie worth seeing. The higher `imdb_score` is better.

![](https://cdn-images-1.medium.com/max/800/1*cVf_Oqoqcba-ezExhIkAUQ.png)

### How to perform a Pandas sort

From the data set above, I have a question **_“What are the 10 most interesting movies to see?”_**

We will need to sort above data set base on `imdb_score`  column with descending order.

Pandas provide function `sort_values()`  which  allows us to sort the data table based on one or multiple columns. And then we could use `head(10)`  to get 10 most interesting movie.

![](https://cdn-images-1.medium.com/max/800/1*xUvBRWmE7S2Grh6bSyNnzw.png)

Now, how do I the most recent film, and then I care about `imdb_score` later.

![](https://cdn-images-1.medium.com/max/800/1*zxy3G9Ok66S3ysos6bikEw.png)

### That’s it