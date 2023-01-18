---
id: tjfocydbokczznvdpyc1r0k
title: In Operator
desc: ''
updated: 1673946188999
created: 1673944439209
---

- IN operator allows to specify multiple values in a where clause
- IN is the short hand for multiple OR operators

```Sql
SELECT * FROM table_name WHERE column IN (values..);
```

>ℹ️ Info
>
>needs to be run on the same column. cant be run on multiple columns.
