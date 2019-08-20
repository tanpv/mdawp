---
layout: default
---

![](https://cdn-images-1.medium.com/max/1200/1*vInvi6XGnRRsmPM7RjXcVw.jpeg)

`apply()`  normally is used to make some change on a column. Let’s load some data for our demo. This is movie data contain 3 columns `movie_title`, `gross`, `movie_imdb_link`.

![](https://cdn-images-1.medium.com/max/800/1*c-RgUyzusVv2QBQ6nyBxGw.png)

### Change gross to a per million unit using apply()

Gross is in dollar units, so it is quite big and hard to read. We want to change `gross` column into a million dollar unit.

Let’s create a simple function which does conversion, then use `apply()`  on column `gross` to convert every value inside to million unit.

![](https://cdn-images-1.medium.com/max/800/1*YbxweInMFQQDfht1dEpguA.png)

### Shorten movie links

Another thing we want to change in the above data set is the IMDB link. You could see all links start with “[http://www.imdb.com/title/](http://www.imdb.com/title/)” so to shorten links, we could remove this part.

We will create a small function to remove “[http://www.imdb.com/title/](http://www.imdb.com/title/)”, then apply that function to every item inside column `movie_imdb_link`.

![](https://cdn-images-1.medium.com/max/800/1*-HJWn1Qab3xdCsFfJ2IK7A.png)

### That’s it

The `apply()`  function means it will execute an external function to all values in a specific column.
