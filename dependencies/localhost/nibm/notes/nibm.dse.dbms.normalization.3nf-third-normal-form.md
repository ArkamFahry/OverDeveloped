---
id: u0tckorg6m3tdccwwvww6we
title: 3nf Third Normal Form
desc: ''
updated: 1674383261260
created: 1673765736892
---

Although [[Second Normal Form (2NF)|nibm.dse.dbms.normalization.2nf-second-normal-form]] relations have less redundancy than those in [[1NF|nibm.dse.dbms.normalization.1nf-first-normal-form]], they may still suffer from update anomalies. If we update only one tuple and not the other, the database would be in an inconsistent state. This update anomaly is caused by a transitive dependency. We need to remove such dependencies by progressing to Third Normal Form (3NF).

A relation is in third normal form, if there is no [[transitive dependency|nibm.dse.dbms.normalization.transitive-dependency]].
 for non-prime attributes as well as it is in second normal form.

- A relation is in 3NF if at least one of the following condition holds in every non-trivial function dependency $P –> Q$:

  - $P$ is a [[super key|nibm.dse.dbms.types-of-keys#Super Key]]. That means right side needs to be a [[super key|nibm.dse.dbms.types-of-keys#Super Key]]
  - $Q$ is a prime attribute (each element of Y is part of some. that [[candidate key|nibm.dse.dbms.types-of-keys#Candidate Key]]). That means the left side needs to be a prime attribute
  
>💫 Short Note
>
>A relation that is in [[First|nibm.dse.dbms.normalization.1nf-first-normal-form]] and [[Second|nibm.dse.dbms.normalization.2nf-second-normal-form]] Normal Form and in which no non-primary-key attribute is transitively dependent on the primary key, then it is in Third Normal Form (3NF).

_

>⚠️ Note
>
> If $P->Q$ and $Q->R$ are two functional dependencies then $P->R$ is called [[transitive dependency|nibm.dse.dbms.normalization.transitive-dependency]].

### How to resolve 3NF anomaly

>💫 Short Note
>
>If a transitive dependency exists, we remove the transitively dependent attribute(s) from the relation by placing the attribute(s) in a new relation along with a copy of the determinant.
