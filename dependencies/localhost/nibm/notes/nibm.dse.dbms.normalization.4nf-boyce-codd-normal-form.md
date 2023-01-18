---
id: nlnbn8ps4lzba1x6vv62w3l
title: 4nf Boyce Codd Normal Form
desc: ''
updated: 1674059875620
created: 1673766304734
---

Boyce–Codd Normal Form (BCNF) is based on functional dependencies that take into account all candidate keys in a relation; however, BCNF also has additional constraints compared with the general definition of [[3NF |nibm.dse.dbms.normalization.3nf-third-normal-form]].

A relation is in BCNF if, $X$ is  [[super key|nibm.dse.dbms.types-of-keys]] for every functional dependency (FD) $X?Y$ in given relation.

>⚠️ Note
>
>A relation is in BCNF, if and only if, every determinant is a Form (BCNF) candidate key.
