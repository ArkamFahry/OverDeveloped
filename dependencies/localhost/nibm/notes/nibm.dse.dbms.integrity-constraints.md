---
id: 4y3o22qoaf1pfkyyvqs4r05
title: Integrity Constraints
desc: ''
updated: 1674311397509
created: 1674300438817
---

## Mainly Constraints on the relational database are of 4 types

1. [[Domain constraints |nibm.dse.dbms.integrity-constraints#1. Domain constraints]]
2. [[Key constraints |nibm.dse.dbms.integrity-constraints#2. key constraints (Uniqueness Constraints)]]
3. [[Entity Integrity constraints |nibm.dse.dbms.integrity-constraints#3. Entity Integrity Constraints]]
4. [[Referential integrity constraints |nibm.dse.dbms.integrity-constraints#4. Referential Integrity Constraints]]

### 1. Domain constraints

- Every domain must contain atomic values(smallest indivisible units) it means composite and multi-valued attributes are not allowed
  
- We perform datatype check here, which means when we assign a data type to a column we limit the values that it can contain

Ex:

- If we assign the datatype of attribute age as int, we can't give it any values other then int datatype

- If we assign the datatype of attribute name as char, we can't give it any values other then char datatype

### 2. key constraints (Uniqueness Constraints)

- Tuple in the relation should be unique

- A relation can have multiple keys or candidate keys(minimal super key), out of which we choose one of the keys as primary key. we have to use the candidate key with less number of attributes.

- NULL values are not allowed in the primary key

### 3. Entity Integrity Constraints

- No primary key can be NULL value, since we use the primary key to identify tuples uniquely

### 4. Referential Integrity Constraints

- This type of constraints is specified between two relations or tables and used to maintain the consistency among the tuples in two relations

- This constraint is enforced through foreign key, when an attribute in the foreign key of relation $R1$ have the same domains as the primary key of relation $R2$, then the foreign key of $R1$ is said to reference or refer to the primary key of relation $R2$
- The values of the foreign key in a tuple of relation $R1$ can either take the values of the primary key for some tuple in relation $R2$, or can take NULL values, but can’t be empty (in simple term if NOT NULL is not specified it can be NULL)
