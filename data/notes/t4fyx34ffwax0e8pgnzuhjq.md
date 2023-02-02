
## DCL means Data Control Language

DCL includes commands such as GRANT and REVOKE which mainly deal with the rights, permissions, and other controls of the database system

EX:

- GRANT - this command gives users access privileges to the database
- REVOKE - this command withdraws the user’s access privileges given by using the GRANT command
  
## Dcl SQL

- ### Creating Logins

- Create Login

```Sql
CREATE LOGIN login_name WITH PASSWORD = password;
```
  
- Select All Logins On Database

```Sql
SELECT
  sp.name AS login,
  sp.type_desc AS login_type,
  CASE
    WHEN sp.is_disabled = 1 THEN 'Disabled'
    ELSE 'Enabled'
  END AS status,
  sl.password_hash,
  sp.create_date,
  sp.modify_date
FROM sys.server_principals sp
LEFT JOIN sys.sql_logins sl
  ON sp.principal_id = sl.principal_id
WHERE sp.type NOT IN ('G', 'R')
ORDER BY create_date DESC;
```

- ### Creating Users

- Create User

```Sql
CREATE USER user_name FOR LOGIN login_name;
```

- Create User With Default Schema

```Sql
CREATE USER user_name FOR LOGIN login_name WITH DEFAULT_SCHEMA = schema_name;
```

- ### Grant Privileges

```Sql
GRANT operations ON entity(object/table) TO user;
```

- ### Revoke Privileges

```Sql
REVOKE operations ON entity(object/table) FROM user;
```

- ### Operations

  - SELECT
    - basic select operation
  - INSERT
    - basic insert operation
  - UPDATE
    - basic update operation
  - DELETE
    - basic delete operation
  - CONTROL
    - all of the above operation that means SELECT, INSERT, UPDATE, DELETE basically access for all database operations
