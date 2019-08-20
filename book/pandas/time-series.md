---
layout: default
---


![Photo by [Andrey Grushnikov](https://www.pexels.com/@andrey-grushnikov-223358?utm_content=attributionCopyText&utm_medium=referral&utm_source=pexels) from [Pexels](https://www.pexels.com/photo/black-and-white-photo-of-clocks-707676/?utm_content=attributionCopyText&utm_medium=referral&utm_source=pexels)](https://cdn-images-1.medium.com/max/1200/1*cmzldMcPVT2TQyIFUc2nmQ.jpeg)
Photo by [Andrey Grushnikov](https://www.pexels.com/@andrey-grushnikov-223358?utm_content=attributionCopyText&utm_medium=referral&utm_source=pexels) from [Pexels](https://www.pexels.com/photo/black-and-white-photo-of-clocks-707676/?utm_content=attributionCopyText&utm_medium=referral&utm_source=pexels)

Pandas provide great tool to working with time series data. Time series data is data which have time related to it. Example of time series data like bitcoin price, stock market, weather.

### Prepare some data

Let load whole time bitcoin history data from [coinmarketcap](https://coinmarketcap.com/). Data contain columns `Date, Open*, High*, Low, Close**, Volume, Market Cap`.Here we have data from 2013 to recently 2019.

![](https://cdn-images-1.medium.com/max/800/1*UcB2JHCdFuJyKzD3Ssr6pg.png)

Let checkout type of each column

![](https://cdn-images-1.medium.com/max/800/1*7UrhQODxoTOMzfq688FSwQ.png)

Currently, `Date` has type `object`. Now before use pandas with all it’s ability to support time series, we must convert `Date` column to `Datetime` type then setting `Date` as index.

![](https://cdn-images-1.medium.com/max/800/1*_8LIHVZo0MkC0d0ViGmyNg.png)

Seem we successful setting `Date` column as index, now we want to sort this index, so data will start from early time. This will make more convenient for selecting data with slice.

![](https://cdn-images-1.medium.com/max/800/1*8gUIS33uBR1OjQWMpcHEWw.png)

### Selecting time series data

After prepare a ready time series data, we could select data for a particular day, for example the final day of 2017 as below.

![](https://cdn-images-1.medium.com/max/800/1*e-iEJq2R15eFiHQqyAD8LA.png)

or select the entire month Dec 2017, then I plot close price for that month. What a history moth 😃

![](https://cdn-images-1.medium.com/max/800/1*FW6BkQgPqjFoGlcWk0c9HQ.png)

or select entire 2019 then plot with close price

![](https://cdn-images-1.medium.com/max/800/1*IXJWEKTS2hoCyyaah3soWA.png)

another powerful feature is selecting with slice, here we select 2 years data with slicing.

![](https://cdn-images-1.medium.com/max/800/1*5haU9ZCnO-C6D2LX7s-CaA.png)

### Resampling

Let say I care about bitcoin price in 2018.

![](https://cdn-images-1.medium.com/max/800/1*-uH9q72y1sa75ihMKhuI9g.png)

We do not want to care about day by day price changing, but we want to know the long term trend. So, we should have a number which could present price for each month. In this case we will get month price by mean of every day inside that month. Pandas provide us a method call `resample` which do exactly that task.

We call `resample` method with `M` parameter so every days which have same month will be group together, then we get mean value.

![](https://cdn-images-1.medium.com/max/800/1*i_a06vvhUmiXliZ7i9NHyg.png)

You could see that now 365 data point for 2018 now become 12 data point (one data point for each month). Now let draw price graph for 2018 after doing monthly resample

![](https://cdn-images-1.medium.com/max/800/1*rk6J6O-2HVLDym-sZPaU-w.png)

So you could see now from graph show up the long term trend, not the price change every day.

Finally let say, we want to resample entire data set by year and draw the trend price.

![](https://cdn-images-1.medium.com/max/800/1*MCI9KBpYco5A2gIEXf3lQg.png)

That it, we have graph with 7 point and each point represent for a year.