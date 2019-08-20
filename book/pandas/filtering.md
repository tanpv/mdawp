---
layout: default
---

![](https://cdn-images-1.medium.com/max/800/1*GpDCH_Ba6I-C3MXG18ikRQ.jpeg)

With data analysis, filtering data is a crucial task. This post will help you understand how to do filtering with pandas.

First, let’s load some data for our demo. This is movie data set which contains 5 columns ‘movie\_title’, ‘director\_name’, ‘imdb\_score’, ‘duration’, ‘genres’.

![](https://cdn-images-1.medium.com/max/800/1*J3QcxP4kS0a3f8ODorILRA.png)

### how filtering works

**_Filter work base on logical operator result — that’s it_**. For example we need to find all movies directed by ‘James Cameron’. Let see follow logical operator on pandas, it returns a series of `True` and `False`.

![](https://cdn-images-1.medium.com/max/800/1*IowDiqt2rR6pZfqF1TcNtQ.png)

Now if we put the result of the above logical inside selection operator, pandas will only select rows where the logical returns `True`.

![](https://cdn-images-1.medium.com/max/800/1*J5DEEBlpuf36tbePtBw2Ug.png)

#### **_what are good movies to see ?_**

IMDB score of a movie represents how people like that movie. So let find out movies with `imdb_score > 9` only. I see ‘The Godfather’ here :)

![](https://cdn-images-1.medium.com/max/800/1*brQW4uS-WD0YmF_mAtT1oQ.png)

#### **_find all movies which duration from 60 mins to 90 mins ?_**

To solve this question, we need to combine 2 logical operators, but the way it works is the same, pandas will select rows which have logical result is `True`.

![](https://cdn-images-1.medium.com/max/800/1*U387khtHMTaVJhUVx79GgA.png)

Now let go further more complicated.

### find all sci-fi movies

First of all let see some data from ‘genres’ column.

![](https://cdn-images-1.medium.com/max/800/1*UAURsZzlUMYOgtNkl10kjQ.png)

Each movie could have multiple genres, so we should create a separate function to check if ‘Sci-Fi’ in genres or not.

![](https://cdn-images-1.medium.com/max/800/1*5E8aVoiFzDkUEW-FpACnHg.png)

The `apply()` function returns a series of `True` or `False` corresponding to a movie is an sci-fi movie or not. Now let’s apply the result of above function to selector operation, we will have final result.

![](https://cdn-images-1.medium.com/max/800/1*FjoLyKZHYRCLCsd8ufcrFg.png)

### so in total how many sci-fi movie we have ?

Just put `sum()` on result of `apply()`  we will have result needed.

![](https://cdn-images-1.medium.com/max/800/1*wOzEou-wp6WdBL55dkPHQw.png)

### that’s it
