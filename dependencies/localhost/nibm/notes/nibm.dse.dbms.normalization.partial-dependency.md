---
id: 4z6kmlesnvekbo6sft2mhhy
title: Partial Dependency
desc: ''
updated: 1673796161288
created: 1673785982686
---

Partial dependency occurs when non-prime attribute is functionally dependant on part of a candidate key

### Lets Understand partial dependency shall we

In order to understand partial dependency, let us first know some basic terminologies with the help of an example.

Consider a relation(table) having four attributes $P,Q,R,S$ having the following dependencies:

$$
P,Q -> S\\
Q -> R
$$

Using $P$ and $Q$, we can derive $S$, and using $Q$, we can derive $R$. Hence, we can say that if we use both $P$ and $Q$ together we can derive all the attributes of the table. i.e, $P,Q,R,S$.(since $P -> P$ and $Q -> Q$ is self explanatory).

We can write $PQ = \{P,Q,R,S\}$, or in simple words, we can say the closures of $P$ and $Q$ give us all the attribute of the relation.. The minimal sets like $PQ$ in a relation(table) that are capable of deriving all the attributes of a relation(table) are called Candidate keys. There can be more than one candidate key in a table.

If an attribute is a part of any candidate key of the relation, then it is called a Primary attribute else, it is said to be a Non-Primary attribute. In the example above, we can say that $P$ and $Q$ are primary attributes, and $R$ and $S$ are non-primary attributes.

We now know the basic definitions required to understand the concept of partial dependency. In the above example, $S$ is dependent on all the primary attributes, i.e.,$P$ and $Q$. If either $P$ or $Q$ are missing, then we cannot derive $S$. In the case of $R$, it is not the same.

Even if $P$, a primary attribute, is missing, we can still derive $R$ using only $S$. Hence, instead of depending totally on the candidate key, $R$ is partially dependent on $Q$, part of a candidate key. This is the concept of partial dependency.

### What Causes Partial Dependency to Occur?

As we saw in the above section, partial dependency occurs whenever a non-prime attribute depends functionally on a part of the given candidate key.

In other words, Partial Dependency occurs when an attribute in a table depends on only a part of the primary key and not the whole key.

A functional dependency denoted as $X→Y$ where
$X$ and $Y$ are an attribute set of a relation, is a partial dependency , if some attribute $A∈X$ can be removed and the dependency still holds.

Let us take an example, consider an example of a College. A student studies in a course, and every student in the college has a unique EnRollNo number.

|Course|EnRollNo|Name|
|---|---|---|
|DSE|CODSE22.2-01|Ashwak|
|CSE|CODSE22.2-02|Dulein|
|DCSD|CODSE22.2-03|Niven|
|DNE|CODSE22.2-04|Nazar|
|BSC|CODSE22.2-05|Arkam|

Suppose you are a student at this college. If a professor asks you to go and give a notebook to the student who has a EnRollNo. CODSE22.2-01, you can quickly identify the student by observing his/her roll. no., i.e.,$CODSE22.2-01$ he is from 2022 Second batch in Diploma In Software Engineering and His student Number is O1

Hence, you can successfully give him/her the notebook. You don't even need to know the Course that s/he is pursuing because you can easily determine it with his/her unique Roll. No.

In other words, if someone provides you with a just the $EnRollNo$, you can quickly tell the student's name. A $EnRollNo$ alone is sufficient to identify or know the student's name. The Name attribute is partially dependent on the $EnRollNo$ attribute.
