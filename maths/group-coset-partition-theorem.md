Group Coset Partition Theorem
=============================

Given a group $G$ and subgroup $H\subseteq G$, it can be shown that each coset of $H$ contains the same number of members as $H$ and the collection of (distinct) cosets of $H$ partition $G$.[^partition]

The Trivial Group
------------------
Consider the case where $\abs{G}=1$. The only subgroup of $G$ is itself, and as $G$ is closed, it is the *trivial group*, i.e. $G = \set{e}$ where $e$ is the identity on $G$. Evidently, any coset of $G$ must also be $G$, and thus must also partition $G$ as $\set{G}$. 

The Trivial Subgroup
--------------------
Let $\abs{H}=1$, for $\abs{G} > 1$. Then $H$ is the trivial subgroup $H=\set{e}$, and each coset of $H$ is the singleton set $\set{a}$ for $a \in G$. It follows that the set $\set{\set{a}:a \in G}$ partitions $G$.

$\abs{H} = \abs{G}$
---
If $\abs{G} > 1$ then $H=G$, and the only coset of $H$ is $G$ (as $G$ is closed). It then holds that the coset $G$ is a partition of $G$.

$1 \lt \abs{H} \lt \abs{G}$
---
<!-- This reminds me of the differential solution proofs -->
Now we consider the case where $\abs{G} > 1$ and $1 < \abs{H} < \abs{G}$. If $\abs{G} = n$, and $\abs{H} = m$ then we may list the members of $H$ as
$$
H = \set{a_1, \,a_2,\, \dots,\, a_{m}}\,,
$$
where $a_1 = e$. For any $a \in G$, the coset $a\circ H$ is
$$
a\circ H = \set{a \circ a_1,\, a \circ a_2,\, \dots,\, a \circ a_m}\,.
$$
Evidently $a \circ H$ cannot contain more than $m$ members. Additionally, for $a \circ H$ to have *fewer* than $m$ members, we must have $a \circ a_i = a \circ a_j$ for some $i,\,j$. This would imply $a^{-1}\pqty{a \circ a_i} = a^{-1}\pqty{a \circ a_j}$, and hence $a_i = a_j$, which we know is not true for a group $H$ of $m$ members. Therefore $\abs{a\circ H}=\abs{H}$.

As $H$ is a *subgroup* of $G$, it contains the identity element $e$. For $a \in G$, it follows that $a \in a\circ H$. Let us assume that for some $b\in G$, $a$ is also a member of the coset $b\circ H$. It follows that there exists some $h_a\in H$ such that 
$$
\tag{a}
a=b\circ h_a\,.
$$
Now consider another element $x \in a\circ H$. One can find another element $h_x \in H$ such that $x = a \circ h_x$. From **(a)** $x$ becomes 
$$
x = b\circ h_a\circ h_x\,.
$$
Given that $H$ is closed (it is a subgroup), $h_a\circ h_x \in H$, and therefore $x \in bH$. It follows that for each $x \in a\circ H$ it holds that $x \in b\circ H$, i.e.
$$
\tag{b}
a\circ H \subseteq b\circ H\,.
$$

Let us now consider $x \in b\circ H$. As before, $\exists h_x \in H$ such that $x = b\circ h_x$. Since **(a)** gives $b=a\circ h_a^{-1}$ we have
$$
x = a \circ h_a^{-1}h_x\,.
$$
Under closure of $H$, we have $x \in a\circ H$. It follows that for each $x \in b\circ H$ it is also true that $x \in a \circ H$, and thus
$$
\tag{c}
b\circ H \subseteq a\circ H\,.
$$

Given **(b)** and **(c\)**, it follows that $a \in a \circ H$ and $a \in b \circ H$ iff. $a\circ H=b\circ H$. In other words, each element of $a\in G$ is a member of only the *distinct* coset formed by $a\circ H$. Evidently, then, the intersection of two distinct cosets (which corresponds to those elements of $G$ in both cosets) must be the empty set $\emptyset$, and thus the distinct cosets of $H$ partition $G$ with  
$$
    \set{a\circ H : a \in G}\,.
$$

<!-- TODO what about auxillary elements? -->

[^partition]: http://ksuweb.kennesaw.edu/~sellerme//sfehtml/classes/math4361/chapter5section1outline.pdf