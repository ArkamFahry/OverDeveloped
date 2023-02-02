
CHECK will be used to set a check constraint on table creation

- table with inline CHECK

```Sql
CREATE TABLE Employee (
    Id CHAR(5) PRIMARY KEY,
    Name VARCHAR(10) CHECK (Name LIKE 'A%'),
    Salary REAL CHECK (Salary BETWEEN 1000 AND 10000),
    Age INT CHECK (Age > 18),
    Dept VARCHAR(10)
);
```

- table with CHECK at the end

```Sql
CREATE TABLE Employee (
    Id CHAR(5) PRIMARY KEY,
    Name VARCHAR(10),
    Salary REAL,
    Age INT,
    Dept VARCHAR(10),
    CHECK (Name LIKE 'A%'),
    CHECK (Salary BETWEEN 1000 AND 10000),
    CHECK (Age > 18)
);
```

- table with named CHECK at the end

```Sql
CREATE TABLE Employee (
    Id CHAR(5) PRIMARY KEY,
    Name VARCHAR(10),
    Salary REAL,
    Age INT,
    Dept VARCHAR(10),
    CONSTRAINT chk_name CHECK (Name LIKE 'A%'),
    CONSTRAINT chk_salary CHECK (Salary BETWEEN 1000 AND 10000),
    CONSTRAINT chk_age CHECK (Age > 18)
);
```

>ℹ️ Info
>
>I f constraint CHECK is created with a name it can be dropped or altered by it's given name
