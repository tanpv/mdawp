---
layout: default
---


![](https://cdn-images-1.medium.com/max/800/1*mcUE5DxuN2FngrJlXK6CHA.jpeg)

Select a subset of data while doing data analysis with pandas is an essential skill which you should master before move on to other things. In this post, I will show you how to select data in a clear and easy way.

For this demo, we will be working with a small version of “IMDB\_movie” data set, which contain only 3 columns: `movie_title`, `director_name`, and `title_year`

![](https://cdn-images-1.medium.com/max/800/1*Y4pdLS2UsoStRHIRJ5fYSA.jpeg)

### Overview

Select a subset of the above data frame could be in one of following cases:

*   select one column (with the `**_._**` operator)
*   select multiple columns (with `[]` operator)
*   select one or multiple rows (with `loc` or `iloc` operator)
*   select one or multiple rows within one or multiple columns (with `loc`  or `iloc`  operator)

We will go to each operator **_. \[\] .loc .iloc_** and see how it could be used.

### `.` operator to select one columns

![](https://cdn-images-1.medium.com/max/800/1*n-n1e2juuEoPlbKF_IWbAg.jpeg)

After load data with the `read_csv()`  function above, all column inside data the frame become its property**_,_** so it is natural to access one column with `.` operator like object access its own property.

![](https://cdn-images-1.medium.com/max/800/1*qVdj2KcDSpqYc6p4OsEcMA.jpeg)

### \[ \] operator to select multiple columns

![](https://cdn-images-1.medium.com/max/800/1*gKym4c2k7MpPPnYleHPbQw.jpeg)

To select multiple columns, you use the `[]` operator and put in columns list, that is why you will see a double `[[]]`

![](https://cdn-images-1.medium.com/max/800/1*Nm_0eGVO-1qkPZqpo2wYGQ.jpeg)

### .loc operator to select multiple rows between multiple columns

Before use `.loc`  we should understand about pandas data frame **_label_**, image below show **_columns label_** and **_rows label_** in a data frame.

![](https://cdn-images-1.medium.com/max/800/1*7gPxoriIkZM4IrEJwsmHew.jpeg)

`.loc` operator uses the following structure to access rows and columns

![](https://cdn-images-1.medium.com/max/800/1*-n5_QSgHncT1UBQNAWRngQ.jpeg)

Let try with an example with one row and one column

![](https://cdn-images-1.medium.com/max/800/1*vZhd9DcbZ62xkusiG3jdgg.jpeg)

Another example to select multiple rows within multiple columns

![](https://cdn-images-1.medium.com/max/800/1*uUiOOW-g1NWuBwYYJ0sfxQ.png)

### .iloc operator to select multiple rows between multiple columns

Befor using `.iloc`,  we should understand about pandas data frame **_position_**.  The image below shows the system of **_row position_** and **_column position._** Imagine each row / column has a position number, and this number starts from 0.

![](https://cdn-images-1.medium.com/max/800/1*0O1iQSLS70XEOU1Z-o_wMw.jpeg)

Not like `.loc`  which works based on `label`**_, _**`.iloc`  select rows and columns based on position system.

![](https://cdn-images-1.medium.com/max/800/1*8ehfA7b09buBZEaR8-50kw.jpeg)

Try with the example below to select one row, one column

![](https://cdn-images-1.medium.com/max/800/1*YjCUtfRP9H3aA5CXm6MK4g.png)

and select multiple rows within multiple columns

![](https://cdn-images-1.medium.com/max/800/1*rzMvelkkmcPMKpLBAvaBDg.png)

### Wrapping Up

Above example show that the way we select rows are the same for **_.loc_** and **_.iloc._** That is because in this case (and normally) the **_label_** and **_position_** for rows are same \[0, 1, 2 …\]

But you should remember that the panda's **_label_** could be reassigned and not use default system with \[0,1,2 …\] and at that time, **_label_** and **_position_** on rows are different.

### That it