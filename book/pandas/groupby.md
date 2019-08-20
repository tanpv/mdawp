---
layout: default
---

`groupby` is one of several powerful functions in pandas. Using `groupby()`  with just one function, we could have answer for a fairly complicated question.

Let say we have a data frame about movies contain 3 columns: “director\_name”, “movie\_title”, “movie\_facebook\_likes”.

![](https://cdn-images-1.medium.com/max/800/1*WcNra2Ed8bjigxU_p0z8vA.jpeg)

### The million dollar question

Suppose we are doing data analysis on the above data table and have a question need to have answer: **_“Based on data above of 3 directors, who has the largest number of Facebook likes?”_**

So let’s think about possible steps to solve the question:

*   Step 1: Go to each row and find all row which has director name is “James Cameron”
*   Step 2: With each row found in step 1, count facebook likes
*   Step 3: Repeat step 1 and 2 for remain directors — “Quentin Tarantino” and “Christopher Nolan”

Have any other better way with pandas?

### Groupby

Pandas has a function called `groupby()`, combining code group together by row which has the same value in ‘director\_name’ column

![](https://cdn-images-1.medium.com/max/800/1*H-fmdJ-I17uRFQCmF3P5hg.png)

We could imagine after `groupby()`  function above, the original table is split into multiple small tables based on each unique value in columns ‘director\_name’.

![](https://cdn-images-1.medium.com/max/800/1*ISmT-jvC8a_xlcqkDBBEgQ.jpeg)

### Apply

After grouping all rows which have the same director\_name, we need to apply  function `sum()`  to accumulate facebook likes for each director. After the function `sum()`  is executed, _a_ new data frame is built which has the index value of ‘director\_name’ column.

![](https://cdn-images-1.medium.com/max/800/1*e7FFpA9RzIWZRAK-wsdL7w.jpeg)
![](https://cdn-images-1.medium.com/max/800/1*lCZmTu7M0IuWFipcO8yVQg.jpeg)

### The Answer

So now we ready to have the answer for the above question, just one more step to **_sort \_values()_** for column ‘movie\_facebook\_likes’. So it seems “**Quentin Tarantino**” is winner.

df\_imdb.groupby('director\_name').sum().sort\_values('movie\_facebook\_likes', ascending=False)

![](https://cdn-images-1.medium.com/max/800/1*_gO2-7kmIQjy_HY8V0tW3g.png)

### That it

Hope you have some fun time with pandas `groupby()`  function, one of very powerful tool.
