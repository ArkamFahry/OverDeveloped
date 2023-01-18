---
id: 808ldgljkgypg0vym3xmkaw
title: Types of Keys
desc: ''
updated: 1674059964499
created: 1673774773938
---

- ## Candidate Key

he minimal set of attributes that can uniquely identify a tuple is known as a candidate key

Ex: Users relation has User_ID, NIC, Email each of these values can be used to uniquely by them selves identify the tuples in the user relation

>ℹ️ Info
>
>- It is a minimal super key.
>- It is a super key with no repeated data is called a candidate key.
>- The minimal set of attributes that can uniquely identify a record.
>- It must contain unique values.
>- It can contain NULL values.
>- Every table must have at least a single candidate key.
>- A table can have multiple candidate keys but only one primary key (the primary key cannot have a NULL value, so the candidate key with NULL value can’t be the primary key).
>- The value of the Candidate Key is unique and may be null for tuple.
>- There can be more than one candidate key in a relation. For Example, STUD_NO is the candidate key for relation STUDENT.
>- The candidate key can be simple (having only one attribute) or composite as well. For Example, {STUD_NO, COURSE_NO} is a composite candidate key for relation STUDENT_COURSE.
>- No, of candidate keys in a Relation are nC(floor(n/2)),for example if a Relation have 5 attributes i.e. R(A,B,C,D,E) then total no of candidate keys are 5C(floor(5/2))=10.

_

>⚠️ Note
>
>In SQL Server a unique constraint that has a nullable column, allows the value ‘null‘ in that column only once. That’s why the STUD_PHONE attribute is a candidate here, but can not be ‘null’ value in the primary key attribute.

- ## Super Key

A set of attributes that can uniquely identify a tuple is known as Super Key

Ex: Student relation Student_No, Phone_Number, (Student_No, Student_Name)

A super key is a group of single or multiple keys that identifies rows in a relation. Attributes in a super key can be NULL

Ex: Student_No + Phone_Number is a super key

>ℹ️ Info
>
>- Adding zero or more attributes to the candidate key generates the super key.
>- A candidate key is a super key but vice versa is not true.

- ## Primary Key

The main key of a relation. selected from the most relevant candidate key according to the criteria. there can be more than one candidate key in relation out of which one can be chosen as the primary key

Ex: Student_No, Student_Phone_No, NIC are candidate keys of the Student relation. But student number is selected as the primary key because it is most relevant for the system where students reside

>ℹ️ Info
>
>- It is a unique key.
>- It can identify only one tuple (a record) at a time.
>- It has no duplicate values, it has unique values.
>- It cannot be NULL.
>- Primary keys are not necessarily to be a single column; more than one column can also be a primary key for a table.

- ## Alternate Key

The candidate key which is other than the primary key is called an alternate key.

Ex: Student_No, Student_Phone_No both these keys will candidate keys for the Student relation but Student_Phone_No will be alternative key (one out of many candidate keys). It is a secondary key.

>ℹ️ Info
>
>- All the keys which are not primary keys are called alternate keys.
>- It contains two or more fields to identify two or more records.
>- These values are repeated.

- ## Foreign  Key

This is key which can take a value if it is only present as a value of a other attribute it will be the foreign key to the attribute which it refers to.  

The relation which is being referenced is called referenced relation and the corresponding attribute is called referenced attribute and the relation which refers to the **referenced relation** is called referencing relation and the corresponding attribute is called **referencing attribute**. The referenced attribute of the referenced relation should be the primary key to it.

Ex: In the relation User User_Role is a foreign key reference to the Role relations primary key

>ℹ️ Info
>
>- It is a key it acts as a primary key in one table and it acts as secondary key in another table.
>- It combines two or more relations (table) at a time.
>- They act as a cross-reference between the tables.
>- For example, DNO is a primary key in the DEPT table and a foreign key DPT in EMP

_

>⚠️ Note
> It may be worth noting that unlike the Primary Key of any given relation, Foreign Key can be NULL as well as may contain duplicate tuples it need not follow uniqueness constraint.

- ## Composite Key

Is Sometime scenarios, a table might not have a single column/attribute that uniquely identifies all the records of a table. In order to uniquely identify rows of a table, combination of two or more columns/attributes can be used.

Ex: User relation can have a composite key of User_Full_Name + Phone_Number bot values combined can identify and access a user

>⚠️ Note
>
> It still can give duplicate values in rare cases. So , we need to find the optimal set of attributes that can uniquely identify rows in a table

_

>ℹ️ Info
>
>- It acts as a primary key if there is no primary key in a table
>- Two or more attributes are used to together to make a composite key.
>- Different combinations of attributes may give different accuracy in terms of identifying the rows uniquely.
