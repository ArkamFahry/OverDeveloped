---
id: f1zwovuh9im3dxhfws0mh6j
title: 2nf Second Normal Form
desc: ''
updated: 1674059337005
created: 1673761287920
---

To be in second normal form relation must be in [[first normal form|nibm.dse.dbms.normalization.1nf-first-normal-form]] and relation must not contain any partial dependencies. A relation will be in 2NF if it has no [[partial dependency|nibm.dse.dbms.normalization.partial-dependency]]

Second normal form is based on the concept of full functional dependency.Second normal for applies to a relation with a composite keys where the relations primary key is comprised of two or more attributes.A relation with a single-attribute primary key is automatically in at least 2NF. A relation that is not in 2NF may suffer from the update anomalies.

A relation is in 2NF if it has No Partial Dependency that means no non-prime attribute (attributes which are not part of any candidate key) is dependent on any proper subset of any candidate key of the table

>ℹ️ Info
>
>A relation that is in First Normal Form and every non primary key attribute is fully functionally dependent on the primary key, then the relation is in Second Normal Form (2NF).

_

>⚠️ Note
>
>If the proper subset of candidate key determines non-prime attribute, it is called [[partial dependency|nibm.dse.dbms.normalization.partial-dependency]] a relation which meets this criteria is not in 2NF

_

>💫 Short Note
>
>If the proper subset of candidate key determines non-prime attribute in a relation it will not be in 2NF

EX:

EX 1:

|Std_Id|Course_No|Course_Fee|
|---|---|---|
|codse21.1-01|DSE|2000|
|codse21.1-02|DCSD|4000|
|codse21.1-01|CSE|1500|
|codse21.1-03|DSE|2000|
|codse21.1-03|DNE|3500|
|codse21.1-02|BSC|2100|

See the above table there is many course having the same fee

- Course_Fee cannot alone decide the value of Course_No or Std_Id
- Course_Fee together with Std_Id cannot decide the value of Course_No
- Course_Fee together with Course_No cannot decide the value of Std_Id
Hence,
- Course_Fee would be a non-prime attribute, as it does not belong to the one only candidate key {Std_Id, Course_No}
- But, Course_No -> Course_Fee this means Course_Fee is dependent on Course_No, which is a proper subset of the candidate key. Non-prime attribute Course_Fee is dependent on a proper subset of the candidate key, which is a partial dependency and so this relation is not in 2NF.

### Lets resolve the above 2NF anomaly

>💫 Short Note
>
>If a partial dependency exists, we remove the partially dependent attribute(s) from the relation by placing them in a new relation along with a copy of their determinant

we need to split the table into two tables such as :

Table 1: Std_Id, Course_No

Table 2: Course_No, Course_Fee

Table 1

|Std_Id|Course_No|
|---|---|
|codse21.1-01|DSE|
|codse21.1-02|DCSD|
|codse21.1-01|CSE|
|codse21.1-03|DSE|
|codse21.1-03|DNE|
|codse21.1-02|BSC|

Table 2

|Course_No|Course_Fee|
|---|---|
|DSE|2000|
|DCSD|4000|
|CSE|1500|
|DNE|3500|
|BSC|2100|

>⚠️ Note
>
>2NF tries to reduce the redundant data getting stored in memory. For instance, if there are 100 students taking DSE course, we don't need to store its Fee as 2000 for all the 100 records, instead once we can store it in the second table as the course fee for DSE is 2000
