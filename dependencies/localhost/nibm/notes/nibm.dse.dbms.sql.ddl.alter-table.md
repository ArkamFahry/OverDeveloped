---
id: kep95l5etxguumnmmb9wffn
title: Alter Table
desc: ''
updated: 1673931105305
created: 1673927590803
---

## Alter tables in the database

- adding a column to a table

```Sql
ALTER TABLE table_name ADD column_name data_type constraint
```

- altering the column constraint to not null

```Sql
ALTER TABLE table_name ALTER COLUMN column_name data_type NOT NULL;
```

- altering adding primary key

```Sql
ALTER TABLE table_name ADD CONSTRAINT key_name PRIMARY KEY(attribute);
```

>⚠️ Note
>
>If the column can nullable need to alter it to be not null before adding primary key alteration

- altering and adding foreign key

```Sql
ALTER TABLE table_name ADD CONSTRAINT foreign_key_name FOREIGN KEY(attribute) REFERENCES referenced_table(attribute);
```

>⚠️ Note
>
>If there is no column to create a foreign key on we need to add a column
