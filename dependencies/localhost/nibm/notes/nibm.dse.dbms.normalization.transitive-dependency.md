---
id: 07zlzc6ukbs90726n9d8mcu
title: Transitive Dependency
desc: ''
updated: 1674047851526
created: 1673882075966
---
When an indirect relationship causes functional dependency it is called Transitive Dependency.

If  $P -> Q$ and $Q -> R$ is true, then $P -> R$ is a transitive dependency.

>💫 Short Note
>
>A dependent is indirectly dependent on determinant in Transitive functional dependency

Consider a relation $R(XYZ)$, where $X$,$Y$ and $Z$ are the attributes of the relation
R. A Transitive dependency exists when you have the following functional dependency pattern,
$X→Y$ and $Y→Z$; therefore, $X→Z$. In other words, a functional dependency is said to be transitive if it is indirectly formed by two [[functional dependencies |nibm.dse.dbms.normalization.full-functional-dependency]].

EX:

Game Studio

|Studio_ID|Studio_Name|Game|Head_Quartes|
|---|---|---|---|
|G1|Ubisoft|Rainbow Six Seige|France|
|G2|Active Vision|Call Of Duty|USA|
|G3|Sucker Punch|Ghost of Tsushima|USA|

- In the above game studio table
  - $Game -> Studio\_Name$ : the Game attributes determine  Studio_Name
  - $Studio\_Name -> Head\_Quartes$ : if we know the Studio_Name then we can determine Head_Quartes
  - $Game -> Head\_Quartes$ : If we know the Game, we can determine the Head_Quartes via the Studio_Name column
- If you take a closer look into the functional dependencies they are indeed forming a pattern
  - $A -> B$ and $B -> C$ then $A -> C$.
  - $A -> Game$, $B -> Studio\_Name$ and $C -> Head\_Quartes$.

### Lets remove the above transitive dependency

- To remove the above transitive dependency first lets consider the above table with three attributes (Studio_ID, Studio_Name, Head_Quartes)

Game Studio

|Studio_ID|Studio_Name|Head_Quartes|
|---|---|---|
|G1|Ubisoft|France|
|G2|Active Vision|USA|
|G3|Sucker Punch|USA|

- The above Game Studio table is not in 3NF because it has the Transitive dependency. Let's see what is it

  - $Studio\_ID ->  Studio\_Name$
  - $Studio\_Name -> Head\_Quartes$

- There for the following dependency exists

  - $Studio\_ID ->  Head\_Quartes$

Lets split the above table into to two tables

- First table - $Game\_Studio (Studio\_ID,  Studio\_Name)$
- Second table - $Studio\_Head\_Quartes (Studio\_Name,  Head\_Quartes)$

Game Studio table

|Studio_ID|Studio_Name|
|---|---|
|G1|Ubisoft|
|G2|Active Vision|
|G3|Sucker Punch|

Studio Head Quartes table

|Studio_Name|Head_Quartes|
|---|---|
|Ubisoft|France|
|Active Vision|USA|
|Sucker Punch|USA|

Now the new Game Studio table and Studio Head Quartes table contains no Transitive dependency and the relation is now in 3NF
