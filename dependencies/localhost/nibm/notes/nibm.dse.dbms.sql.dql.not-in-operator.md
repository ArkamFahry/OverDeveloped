---
id: 6d2s8oup0x6va011nlzl5kj
title: Not in Operator
desc: ''
updated: 1673945946260
created: 1673945320788
---

NOT IN lets you compare multiple values like [[IN|nibm.dse.dbms.sql.dql.in-operator]] but NOT LIKE return the values which doesn't match the given criteria

```Sql
SELECT * FROM table_name WHERE column NOT IN (values..);
```

>ℹ️ Info
>
>needs to be run on the same column. cant be run on multiple columns.