---
layout: default
---


![](https://cdn-images-1.medium.com/max/2560/1*DBUfEEyPFfGXaEwhctEOjA.jpeg)

Let loading some data into a Pandas data frame

![](https://cdn-images-1.medium.com/max/800/1*qC9T0lqozmdXNxwwphTASQ.png)

Now after loading data from an external file into a data frame, Pandas provides us some properties and functions to understand data at a high level.

### Number of Rows and Columns

Pandas data frame provides a property name `shape`,  which allows us to know how many rows and how many columns are inside the data table

![](https://cdn-images-1.medium.com/max/800/1*qUgJtCoMbbUlcHvFCv93bQ.png)

### Columns Name

Sometimes we need to know the name of each column, and the data frame has a property called `columns`  provide us name of all columns.

![](https://cdn-images-1.medium.com/max/800/1*ssjhdlwL4Gu2JaNp2Qg1UA.png)

### Sample top rows

`head()`  provides some sample rows from the top of the table. If you don’t provide a number to the function, the default rows to show is 5.

![](https://cdn-images-1.medium.com/max/800/1*FB6dSlb3nOokaVpuGvpVSA.png)

### Sample end rows

Similar to `head()`, the function `tail()` provides rows at the bottom of the table.

![](https://cdn-images-1.medium.com/max/800/1*F9JZ1YsV4Imyjb_D4Lx2_g.png)

### Overview Columns Info

To show number of value in each column and column data type, data frames have the function `info()`.

![](https://cdn-images-1.medium.com/max/800/1*Nu2zh0BaFrgCsLFXHcK3Eg.png)

From the above information, we could see that some missing data happens in column ‘director\_name’ and ‘title\_year’ due to its number of values smaller than ‘movie\_title’

### Overview Statistics

On columns where the type is a number, data frames have a function called `describe()`  which basically print out common statistics for the column. This helps us have an overview of how values are distributed.

![](https://cdn-images-1.medium.com/max/800/1*r6SkPeZsT6-OKW0oOox_yQ.png)

### That’s it