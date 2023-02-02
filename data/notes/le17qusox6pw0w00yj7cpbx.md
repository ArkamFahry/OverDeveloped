
## Create table

```Sql
CREATE TABLE table_name (
    Column_name Data_type Constraint and Check
);
```

Ex:

```Sql
CREATE TABLE Student (
    Id INT IDENTITY(1, 1),
    Name VARCHAR(255) NOT NULL,
    Email VARCHAR(255) NOT NULL,
    Password VARCHAR(255) NOT NULL,
    Gender VARCHAR(10) DEFAULT 'male',
    Address VARCHAR(255),
    CONSTRAINT user_pk PRIMARY KEY(Id) 
);
```

>⚠️ Note
>
>- IDENTITY is used to represent an auto increment Id
>- DEFAULT is used represent a default value in INSERT if its Not Defined or NULL

### Ways of defining primary key

- First method - Inline primary key definement

```Sql
CREATE TABLE Student (
    Id INT PRIMARY KEY,
    Name VARCHAR(255) NOT NULL,
);    
```

- Second method - Defining at the end

```Sql
CREATE TABLE Student (
    Id INT IDENTITY(1, 1),
    Name VARCHAR(255) NOT NULL,
    CONSTRAINT PRIMARY KEY(Id) 
);
```

- Third method - Defining at th end with a primary key name

```Sql
CREATE TABLE Student (
    Id INT IDENTITY(1, 1),
    Name VARCHAR(255) NOT NULL,
    CONSTRAINT user_pk PRIMARY KEY(Id) 
);
```

As shown above primary key has a name user_pk so this can be used to manage the primary key by its name.

Ex:

```Sql
ALTER TABLE Student DROP CONSTRAINT user_pk;
```

As shown above the primary key constraint can be dropped using its defined constraint name.
