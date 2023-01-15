---
id: yy2wmuifbidt7x1ne05lyzx
title: First Normal Form 1NF
desc: ''
updated: 1673757121177
created: 1673711892787
---

If a relation contains any type of [[multi value|nibm.dse.dbms.normalization.types-of-attributes#Multi value attributes]] or [[composite attributes|nibm.dse.dbms.normalization.types-of-attributes#Composite attribute]] it is violation of **first normal form (1NF)**. The relation is in first normal form if it does contain any [[multi value|nibm.dse.dbms.normalization.types-of-attributes#Multi value attributes]] or [[composite attributes|nibm.dse.dbms.normalization.types-of-attributes#Composite attribute]]. In simple terms a relation is in first normal form if every attribute in that relation is singled valued atomic attribute.

### A relation in 1NF

- There is only single valued attributes
- Attribute domain does not change
- There is a unique name for every attribute/column

Ex:

Ex 1:

User Table

|ID|Name|Phone_Number|
|---|---|---|
| 1|John|011231234, 0113322424|
| 2|Logan|011231234, 0113322424, 077341234|
| 3|Paul|011231234, 0113322424|

In the above table Phone_Number has multiple values this means it is a [[multi value attribute|nibm.dse.dbms.normalization.types-of-attributes#Multi value attributes]] so this is not in 1NF form.

Ex 2:

User Table

|ID|Name|Phone_Number|
|---|---|---|
| 1|John|011231234|
| 2|Logan|011231234|
| 3|Paul|011231234|

In the above table Phone_Number has a single atomic value so the above table is in 1NF

## How to resolve a 1NF anomaly

- ### Multi value attribute resolution example

User Table

|ID|Display_Name|Phone_Number|
|---|---|---|
| 1|John|011231234, 0113322424|
| 2|Logan|011231234, 0113322424, 077341234|
| 3|Paul|011231234, 0113322424|

Lets resolve the above [[multi value|nibm.dse.dbms.normalization.types-of-attributes#Multi value attributes]] anomaly

User Table

|ID|Display_Name|
|---|---|
| 1|John|
| 2|Logan|
| 3|Paul|

above table [[multi value attributes |nibm.dse.dbms.normalization.types-of-attributes#Multi value attributes]] Phone_Number has been omitted and extracted to a new table which is shown below

User_Phone_Number Table

|ID|Phone_Number|
|---|---|
| 1|011231234|
| 1|0113322424|
| 2|011231234|
| 2|0113322424|
| 2|077341234|
| 3|011231234|
| 3|0113322424|

As show in the above table User table ID has been copy pasted to the new relation and th Phone_Number column has cut pasted to the new relation and all the values have been distributed into single atomic values

- ### Composite value attribute resolution example

Student Table

|ID|Age|Full_Name|
|---|---|---|
| 1|12|John Fitzgerald Kennedy|
| 2|13|Maria Eduarda Hoffmann|
| 3|14|Theodore Charles Kyle|

Lets resolve the above [[composite value|nibm.dse.dbms.normalization.types-of-attributes#Composite attribute]] anomaly

Student Table

|ID|Age|
|---|---|
| 1|12|
| 2|13|
| 3|14|

above table [[composite value attribute|nibm.dse.dbms.normalization.types-of-attributes#Composite attribute]] Full_Name has been omitted and extracted to a new table which is shown below

Student_Full_Name Table

|ID|Given_Name|Middle_Name|Family_Name|
|---|---|---|---|---|
| 1|John|Fitzgerald|Kennedy|
| 2|Maria|Eduarda|Hoffmann|
| 3|Theodore|Charles|Kyle|

As show in the above table User table ID has been copy pasted to the new relation and th Full_Name column has cut pasted to the new relation as three columns Given_Name, Middle_Name, Family_Name and all the values have been distributed into single atomic values
