
NOT IN lets you compare multiple values like [[IN|nibm.dse.dbms.sql.dql.in-operator]] but NOT LIKE return the values which doesn't match the given criteria

```Sql
SELECT columns... 
FROM table_name 
WHERE column NOT IN (values..);
```

>ℹ️ Info
>
>needs to be run on the same column. cant be run on multiple columns.
