Group Coset Partition Theorem
=============================

Given a group $G$ and subgroup $H\subseteq G$, it can be shown that each coset of $H$ contains the same number of members as $H$ and the collection of (distinct) cosets of $H$ partition $G$.[^partition]

<!-- TODO: prove stmt 1. -->

As $H$ is a *subgroup*, it contains the identity element $e$. For $a \in G$, it follows that $a \in a\circ H$. Let us assume that for some $b\in G$, $a$ is also a member of the coset $b\circ H$. It follows that there exists some $h_a\in H$ such that 
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

Given **(b)** and **(c\)**, it follows that $a \in a \circ H$ and $a \in b \circ H$ iff. $a=b$. In other words, each element of $a\in G$ is a member of only the coset formed by $a\circ H$, and thus the cosets $a\circ H \forall\, a \in G$ partition $G$. 

<!-- TODO what about auxillary elements? -->

[^partition]: http://ksuweb.kennesaw.edu/~sellerme//sfehtml/classes/math4361/chapter5section1outline.pdf