---
layout: default
---


![](https://cdn-images-1.medium.com/max/1200/1*ENlg3jR5TQ6PBnOE_IFABg.jpeg)

The first step to do data analysis is loading data from an external file into pandas DataFrame. Pandas provides support for many different file types as the following image shows:

![](https://cdn-images-1.medium.com/max/800/1*l2jzZoNxMoluT32K63LBYw.jpeg)

### Load a csv file

A csv uses commas to separate data between columns.

![](https://cdn-images-1.medium.com/max/800/1*PbY7thkMPFajju1V6mc1MA.png)

To load data from a csv, pandas provide function called `read_csv()`_,_ this function requires to put in the path to the csv file

```python
df_csv = pd.read_csv('./data/IMDB/Movie/3columns.csv')  
df_csv.head()
```

then we will have below result

![](https://cdn-images-1.medium.com/max/800/1*7-kFpFb_D3KEnKjlsMytyQ.jpeg)

### Loading an Excel file

Pandas provide function `read_excel()`  to read data from excel.

![](https://cdn-images-1.medium.com/max/800/1*-UyaYEcfYYROYYYe_thOHw.jpeg)

### Loading a JSON file

Suppose we have JSON data like below

![](https://cdn-images-1.medium.com/max/800/1*9QxHeCr9OfdE8FmYURV_IQ.jpeg)

Pandas provide function `read_json()`  to read data from json file.

![](https://cdn-images-1.medium.com/max/800/1*NBXTd1rKpfLs53EbYVuF9Q.jpeg)

### Loading an HTML file

If we have a table data which format in .html

![](https://cdn-images-1.medium.com/max/800/1*aL_H2TzPPkML6bgnmCw2Bg.jpeg)

The above data could be load with `read_html()`  function

![](https://cdn-images-1.medium.com/max/800/1*7mAGs57Sw5Qc7DRJYUWrMA.jpeg)

### That’s it