---
id: qj2y5yce8g8cpvxll9jxy0y
title: Nested Query
desc: ''
updated: 1674121052766
created: 1674120080541
---

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
