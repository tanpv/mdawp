---
layout: default
---


![](https://cdn-images-1.medium.com/max/800/1*bJAfxV4qB-R6ajA8GdSKQA.jpeg)

Merge in pandas means **_combine data from 2 data tables to create a new table_**.

Let’s load some data for our demo. Suppose we have 2 tables, `customer` and `order`, and the tables are linked by a column `customer_id` as below.

![](https://cdn-images-1.medium.com/max/800/1*aElEbNtgAoXTucKSLocZzg.png)

### Merge to find the most valuable customer

From the 2 data tables, we want to find out who spent the most. You could see that:

*   James Madison, James Monroe does not exist in the orders table
*   Order with `id` 5, 6 does not exist in the customers table

We want to form a new table which data exists in both tables. Pandas provides a function called `merge()` to handle this situation.

Let see some parameters inside `merge` function

*   `left`, `right` refers to 2 tables which will be merged
*   `on` refer to the column which needs to exist in both tables
*   `how` refer to the way merge happen. In this case we want `customer_id` which exist on both tables, so we use `inner`

![](https://cdn-images-1.medium.com/max/800/1*2DZI6T8YXiuuu0Kr0xaUIA.png)

For the final step, use `groupby` on `customer_id` then `sum` on `amount` column to find the answer.

![](https://cdn-images-1.medium.com/max/800/1*8dk6O1qvGQSlkLMVlyAy6Q.png)

### That’s it