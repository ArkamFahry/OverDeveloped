
```Sql
SELECT columns...
FROM table_name
WHERE columns... operator (
    SELECT columns...
    FROM table_name
    WHERE columns...
)
```

>⚠️ Note
>
>Sub query needs to be in the right hand side of the operation
