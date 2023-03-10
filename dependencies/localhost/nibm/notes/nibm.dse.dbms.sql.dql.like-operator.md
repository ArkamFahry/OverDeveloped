---
id: k49m8nh5v94kdxi2j9h92gl
title: Like Operator
desc: ''
updated: 1674044502854
created: 1673944797879
---
LIKE is a string comparison operator

- '%' :- replaces arbitrary number of characters

- Select by the starting letter

```Sql
SELECT columns... 
FROM table_name 
WHERE column_name LIKE 'letter%';
```

- Select by the ending letter

```Sql
SELECT columns... 
FROM table_name 
WHERE column_name LIKE '%letter';
```

- Select by letter any where middle of the value

```Sql
SELECT columns... 
FROM table_name 
WHERE column_name LIKE '%letter%';
```

- '_' :- replaces single characters

- Select by a single letter match

```Sql
SELECT columns... 
FROM table_name 
WHERE column_name LIKE '_letter%';
```

```Sql
SELECT columns... 
FROM table_name 
WHERE column_name LIKE '__letter%';
```
