---
id: 07zlzc6ukbs90726n9d8mcu
title: Transitive Dependency
desc: ''
updated: 1673939178982
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
|G1|Ubisoft|Assassins Creed|France|
|G2|Active Vision|Call Of Duty|USA|
|G3|Sucker Punch|Ghost of Tsushima|Japan|

- In the above game studio table
  - $Game -> Studio\_Name$ : the Game attributes determine  Studio_Name
  - $Studio\_Name -> Head\_Quartes$ : if we know the Studio_Name then we can determine Head_Quartes
  - $Game -> Head\_Quartes$ : If we know the Game, we can determine the Head_Quartes via the Studio_Name column
- If you take a closer look into the functional dependencies they are indeed forming a pattern
  - $A -> B$ and $B -> C$ then $A -> C$.
  - $A -> Game$, $B -> Studio\_Name$ and $C -> Head\_Quartes$.

### Lets remove the above transitive dependency


