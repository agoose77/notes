Group
=====

A group $(G,\circ)$ is a [set](set.md) $G$ combined with a binary operation $(\circ)$ which combines two elements of the set to produce a third element, whilst satisfying the four [group axioms](#Group-Axioms). 
The group may sometimes be referred to by its _underlying set_ directly, e.g. $G$. 

A group $H$ is called a *subgroup* of $G$ (denoted $H\subseteq G$) iff. $H$ is a group and its elements are a subset of the elements of $G$.

Axioms
------

|       Name       |                         Definition                          |
| :--------------: | :---------------------------------------------------------: |
|  Associativity   | $$\forall a,b,c\in G, (a\circ b)\circ c=a\circ (b\circ c)$$ |
|     Closure      |             $$\forall a,b\in G, a\circ b\in G$$             |
| Identity Element |    $$\exist e\in G:\forall a\in G, e\circ a=a\circ e=a$$    |
| Inverse Element  |   $$\forall a\in G, \exists b\in G:a\circ b=b\circ a=e$$    |


Morphisms
---------
Homomorphism
  ~ A map between groups that respects the group structure, i.e.
  $$
      \phi\colon G_1\rightarrow G_2
  $$ is a homomorphism iff.
  $$
      \forall\,a,b\in G_1,G_2 : \phi(a\circ b) = \phi(a)\circ\phi(b)\,,
  $$
  where $\circ$ is the binary operation of the respective group.
  
Isomorphism
  ~ A [bijective](map.md#Relations) group homomorphism, represented by $G_1\cong G_2$. 


Generators
----------
The generators of a group are a set of elements from which all other elements can be generated through the group multiplication law.[^group-theory] Let $\tilde{G}$ be the generators of group $G$, then
$$
G = \set{(u\circ v):u,v\in \tilde{G}}\,.
$$
 The minimal number of elements which generate $G$ (i.e. the order of the minimal $\tilde{G}$) is called the *rank* of $G$.

Conjugacy
---------
Two elements $a,b\in G$ are conjugate if there exists an element $g\in G$ such that $g\circ a\circ g^{-1} = b$.[^group-theory] In this manner, $a$ and $b$ are conjugate of one another. This forms an [equivalence class](equivalence-class.md) of $a$ given by
$$
\bqty{a} = \set{g\circ a\circ g^{-1} : g \in G}\,.
$$
<!-- TODO prove this -->
The number of distinct conjugacy classes of the group $G$ is called the *class number of $G$*.

Centre
--------
The centre $Z$  of a group $G$ is the subset of elements which commute with *all elements of the group*, given by 
$$
    Z(G) = \set{z \in G : \forall g \in G: z\circ g = g \circ z}\,.
$$

Order
-----
Order of a Group
    ~ The order of a group $G$ denoted $\abs{G}$ counts the number of elements in the group.[^group-theory] 

Order of a Group Element
    ~ The order of a group *element* $g\in G$ denoted by $\abs{g}$ is the smallest integer for which $g^n = e$, where $e$ is the identity of the group, and $g^n$ is given by 
$$
\begin{aligned}
g^1 &= g\\
g^2 &= (g\circ g^1)\\
g^3 &= (g\circ g^2)\\
&\;\;\vdots\\
g^n &= (g\circ  g^{n-1})\\
\end{aligned}\,.
$$

Presentation
------------
A group may be specified by its *presentation* $\braket{S}{R}$ comprised of a set $S$ of generators and set $R$ of relations amongst those generators. A presentation may describe several groups, and thus $\braket{S}{R}$ is taken to be the presentation of $G$ if $G$ is the *largest group* which satisfies the presentation.[^presentation]

Consider the following trivial example[^group-calculator]:  
![](presentation-simple.png)

In this diagram, each element of $g\in G$ is assigned a vertex. Let $\tilde{G}=\set{h,v}$ be the set of (horizontal/vertical) flip generators. Each generator $\tilde{g}\in\tilde{G}$ is assigned a colour.  
It can be seen that a horizontal followed by vertical flip produces $e\rightarrow h\circ e \rightarrow v\circ (h\circ e)$. Equally, the reverse ordered transformation $e\rightarrow v\circ e \rightarrow h\circ (v\circ e)$ ends up at the same vertex. This introduces the relation 
$$
    v\circ h = h\circ v\,.
$$
Additionally, repeated application of the a generator leaves the original element unchanged, i.e.
$$
    v\circ v = h\circ h = e\,,
$$
where $e$ is the identity element. The presentation for this group is
$$
    V_4 = \braket{v,h}{v\circ v=e,h\circ h=e, v\circ h = h\circ v}
$$


Coset
-----
Given a subgroup $H\subseteq G$, the *left*-coset $gH$ for each element $g\in G$ is defined as
$$
g\circ H = \set{g\circ h : h \in H}\,.
$$
Analogously, one can also define the *right*-coset.
<!-- It seems that frequently people choose additive or multiplicative notation instead of the explicit `\circ` notation, but I prefer the explicit form. -->

[It can be shown](group-coset-partition-theorem.md) that the cosets of $H$ [partition](set.md#Partition) the group $G$. Additionally, the left/right cosets form an [equivalence class](equivalence-class.md) on $G$. Let us define the equivalence relation as $x \sim y \iff x^{-1} \circ y \in H$ for $x,\,y \in G$. 
1. Reflexivity  
$x \sim x = x^{-1}\circ x = e \in H$.
2. Symmetry  
If $x \sim y$ then $x^{-1}\circ y \in H$. As $H$ is a subgroup, it follows that $\pqty{x^{-1}\circ y}^{-1} \in H$, i.e. $y \sim x$.
3. Transitivity  
If $x \sim y$ and $y \sim z$ then $x^{-1}\circ y \in H$ and $y^{-1}\circ z \in H$. From closure of $H$, $\pqty{x^{-1}\circ y } \circ \pqty{y^{-1}\circ z}\in H$, which under associativity gives $x \sim y$.

The equivalence relation is equivalent to $x \sim y \iff y \in x H$. It follows that
$$
\bqty{x} = x\circ H\,.
$$

### Lagrange's Theorem
Lagrange's Theorem states that for any subgroup $H$ of $G$, the order of $H$ divides the order of $G$. Since the left-cosets of $G$ form a partition of $G$, so too do the equivalence classes. It follows that
$$
\abs{G} = \abs{g_1\circ H} + \abs{g_2\circ H} + \dots + \abs{g_n\circ H}\,.
$$
[It can be shown](group-coset-partition-theorem.md) that $\abs{g_i H} = \abs{H}$, and therefore$\abs{G} = n\abs{H}$.
<!-- TODO: Group action -->

Action
------
The action of a group $G$ is a map of the group on a set $X$ compatible with the group structure, i.e. let $\phi\colon G\times X \rightarrow X$, where we shall write $\phi(g, x)\rightarrow g\rhd x$ for $g\in G\,, x\in X$.

$\phi$ is the group action iff.[^wiki.action]
1. Identity  
$e\rhd x = x$
2. Compatibility  
$\pqty{g_1 \circ g_2}\rhd x = g_1 \rhd \pqty{g_2\rhd x}$ for $g_1, \,g_2 \in G$.

Examples of the group action include the *trivial action* $g\rhd x = x$, or $G$ acting upon itself ($X=G$) by multiplication ($g\rhd x = g\circ x$) or conjugation $g\rhd x = g\circ x \circ g^{-1}$.[^soq]

The group action is a *homomorphism*. Let $\phi_g(x) = g\rhd x$ . If $Q(X)$ is the set of all functions which are [bijections](group-action-is-bijective.md) of $X$ onto itself, then $\phi_g \in Q(X)$. Now, we consider whether the group action respects the group structure. To ease subsequent expressions, we may define the map $\mu(g) = \phi_g$. Given $x \in X$, we have
$$
\begin{aligned}
    \mu(g_1\circ g_2)(x) 
        &= \phi_{g_1\circ g_2}(x)\\
        &= g_1\rhd g_2 \rhd x\\
        &= g_1 \rhd \phi_{g_2}(x)\\
        &= \phi_{g_1}(\phi_{g_2}(x))\,,
\end{aligned}
$$ 
for $g_1, \,g_2 \in G$. If we define the group operation on $Q$ to be the function composition operator $\pqty{f \circ g}(x) = f(g(x))$, then finally $$\mu(g_1\circ g_2) = \mu(g_1)\circ \mu(g_2)\,.$$

Examples
---------

### Abelian Groups

An Abelian Group (or commutative group) is a group in which the result of applying the group operation does not depend upon the order of the elements upon which it operates, e.g. $$a\circ b=b\circ a$$

An example of Abelian groups is the integers under addition $(\mathcal{Z},\circ +)$ as
$$
    1+2 = 2+1\,.
$$



[^group-theory]: https://www2.ph.ed.ac.uk/~rzwicky2/SoQM/romanSoQM_2015.pdf
[^group-calculator]: http://www.math.clemson.edu/~macaule/classes/m19_math4120/slides/math4120_lecture-1-04_h.pdf
[^presentation]: https://www.youtube.com/watch?v=bjytiO5kRjw
[^lie]: https://homepage.univie.ac.at/harold.steinacker/Liegroups2010-part1.pdf
[^soq]: https://www2.ph.ed.ac.uk/~rzwicky2/SoQM/romanSoQM_2015.pdf
[^wiki.action]: https://en.wikipedia.org/wiki/Group_action#Definition