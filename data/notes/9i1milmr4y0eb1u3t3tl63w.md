
A functional dependency denoted as $X→Y$ where $X$ and $Y$ are an attribute set of a relation, is a full dependency , if all the attributes present in $X$ are required to maintain the dependency.

Ex:

In the relation $PQR->S$, attribute $S$ is fully functionally dependent on $PQR$  and not on any proper subset of $PQR$. That means that subsets of $PQR$ like $PQ$, $QR$, $P$, $Q$, etc cannot determine $S$.

### Lets Understand full functional dependency shall we

Let us take an example, consider an example of a school. A student studies in a class, and in each class, every student has a unique StdNo number (key point StdNo is globally not unique it is only unique in the Class domain).

|Class|StdNo|Name|
|---|---|---|
|10|11|Ashwak|
|9|32|Niven|
|9|17|Dulein|
|8|32|Mr.Nobody|

Suppose you are a student at this school. If a teacher asks you to go and give a notebook to the student who has a StdNo. 32, you will get confused. Then you will ask the teacher to tell you about the class in which s/he is studying. You can then quickly identify the student and successfully give him/her the notebook.

In other words, if someone provides you with a class and the StdNo number, you can quickly tell the student's name. A class or a StdNo number alone is insufficient to identify or know the student's name. The Name attribute is fully dependent on the Class and StdNo attribute.

**Conclusion**

$Class,StdNo -> Name$

So $Name$ is fully functionally dependent $Class,StdNo$ 