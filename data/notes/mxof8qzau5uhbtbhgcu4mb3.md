
The HAVING clause was added to SQL because the WHERE keyword cannot be used with aggregate functions

```Sql
SELECT columns...
FROM table_name
WHERE condition
GROUP BY columns...
HAVING condition -- Acts as a where clause in a aggregate functions
ORDER BY columns...;
```
