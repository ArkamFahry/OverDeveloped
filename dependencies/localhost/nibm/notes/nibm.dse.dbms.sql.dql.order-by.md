---
id: ppwguphjtjauitx9wa7wcn4
title: Order By
desc: ''
updated: 1674045155761
created: 1673947713318
---

- Ordering of result is using ORDER BY
  - Using ORDER BY clause &
  - ASC (default) and DESC clause

- There are two ways of ordering
  - ASC - ascending order
  - DESC - descending order

- The ORDER BY keyword is used to sort the result-set in ascending or descending order.

- The ORDER BY keyword sorts the records in ascending order by default. To sort the records in descending order, use the DESC keyword.

```Sql
SELECT columns... 
FROM table_name 
ORDER BY column ... ASC|DESC;
```

- ORDER BY several columns example

```Sql
SELECT columns... 
FROM table_name 
ORDER BY column1, column2, ... ASC|DESC;
```

>ℹ️ Info
>
>Multiple columns can be used to order the retrieving data in a select query

- ORDER BY several columns example with both ascending ( ASC ) and descending ( DESC )

```Sql
SELECT columns.. 
FROM Customers
ORDER BY columns.. ASC, columns.. DESC;
```

>ℹ️ Info
>
>Multiple columns can be used to order the retrieving data in a select query with both ASC and DESC order
