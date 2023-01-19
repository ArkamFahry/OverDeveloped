---
id: ywixz2xrlk7f14tuquxl8lz
title: Group By
desc: ''
updated: 1674110573577
created: 1674045198843
---

- The GROUP BY statement groups rows that have the same values into summary rows.

- The GROUP BY statement is often used with aggregate functions ( COUNT(), MAX(), MIN(), SUM(), AVG() ) to group the result-set by one or more columns.

- Produce one tuple for every group by applying aggregation  

```Sql
SELECT columns...
FROM table_name
WHERE condition
GROUP BY columns...
ORDER BY columns...;
```

>⚠️ Note
>
>WHERE clause can`t be used after aggregate function GROUP BY we need to use [[HAVING|nibm.dse.dbms.sql.dql.having]] clause
