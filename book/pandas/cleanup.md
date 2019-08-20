---
layout: default
---

![](https://cdn-images-1.medium.com/max/1200/1*wY7lFOA5FQQfuaR2JRip-A.jpeg)

With data analysis or machine learning project, cleanup and preparing data could take a lot of time. This article want to show you how to cleanup data in easy way with pandas.

Clean up data normally mean we do following things :

*   Rename columns so it is easier to read or remember
*   Drop columns that you not care about in your analysis
*   Handle missing data
*   Handle duplicate data
*   Modify column data

Let prepare some data before start our journey, following code load some data from imdb csv file and show up 3 first rows.

![](https://cdn-images-1.medium.com/max/800/1*K7-YYwhKTE36g1fIMyj-cw.jpeg)

### Rename columns

Current columns name seem messy. It contain upper lower case but not follow rule. It also contain space between words, this will not allow you to access column with dot (.) operator.

So at this step we will put all columns name to lower case and replace space with under score.

Pandas allow us to access columns string name with **_.str_** then we can call many kind of function which will manipulate string.

So we have following code and result

![](https://cdn-images-1.medium.com/max/800/1*GiXA_XqzdjWawNluAbT4ZA.jpeg)

### Drop columns

Some time we want to drop columns which not related to analysis result, for example in this data we want to remove ‘director\_name’ column.

Data frame have function **_drop()_** help to drop a list of columns, **_inplace_** parameter mean result is stored right in to **_df\_imdb_**

![](https://cdn-images-1.medium.com/max/800/1*uiUpjwIm1SbSHKbaU4TK9Q.jpeg)

### Handle missing data

Missing data mean no have any value at a specific cell inside data set. Example in follow table, no have duration and title\_year value for star war movie. In pandas missing value is shown up as **_NAN_**

![](https://cdn-images-1.medium.com/max/800/1*WYhj5q_dedonbMa0bqIO3g.jpeg)

To detect missing data, pandas provide 2 functions which are same, they are **_isnull()_** and **_isnan() ._** Run these function again data frame , it return **_True_** or **_False_** for each cell to tell that cell is missing value or not

![](https://cdn-images-1.medium.com/max/800/1*kRkBVO8Ugn4l5JvmK6zmFQ.jpeg)

Now to calculate missing value happen in each columns, we could apply the **_sum()_** function. Note that with **_sum()_** function on boolean value, True = 1 and False = 0

![](https://cdn-images-1.medium.com/max/800/1*6Y-NZYLanc-4SK0gFN6ppA.jpeg)

That it, now we know that have 15 missing value in duration column and 108 missing value on title\_year.

Now we know about missing value and number of missing, normally have 2 following ways to handle missing data

#### Method 1, remove row which contain missing data

Following code, remove all row which missing value for _‘duration’_ column.

![](https://cdn-images-1.medium.com/max/800/1*Jkhmvgr1CjFOB9xZJRSpyQ.jpeg)

#### Method 2, fill value with fillna

In this example we calculate mean value for each column, then fill NAN cell with that mean.

![](https://cdn-images-1.medium.com/max/800/1*_wPL9djQGBcA3J991hOAPQ.jpeg)

### Handle duplicate data

Duplicate mean we have rows which value in columns are all the same. To detect duplicate rows, pandas provide function **_duplicated()_** which will return False if row no have duplicate and True if have, so result of **_duplicated()_** function is a series of True or False value.

![](https://cdn-images-1.medium.com/max/800/1*8_U8EHMvNODXMOkQSG19mg.jpeg)

So to calculate have how many rows duplicated, we use **_sum()_** on series of Boolean value.

![](https://cdn-images-1.medium.com/max/800/1*g4XpaeLT4mht22h_tFgX0A.jpeg)

To remove duplicate rows, pandas provide function call **_drop\_duplicates._** This function has parameter call **_‘keep’_**

*   keep=’first’ mean keep the first in rows of duplicate
*   keep=’last’ mean keep the last in rows of duplicate
*   keep=False mean drop all duplicates

![](https://cdn-images-1.medium.com/max/800/1*eaKpM1dGvYcR3RJcVL3XiQ.jpeg)

### Modify column data

Some time data from column need to be modify, for example column ‘title\_year’ contain year number but it show up in float data type

![](https://cdn-images-1.medium.com/max/800/1*gOU4c9lcJz8aDUHT-_tLLA.jpeg)

So below code will using apply function to convert data from float data type to int data type as we expected for year number.

![](https://cdn-images-1.medium.com/max/800/1*0PP6x7Zj9nRx-4ciHwOfKw.jpeg)

### That it

We already go through some common task when doing clean data set.