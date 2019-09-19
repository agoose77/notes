Group
=====

A group is a [set](set.md) $G$ combined with a binary operation $(\circ)$ which combines two elements of the set to produce a third element, whilst satisfying the four [group axioms](#Group-Axioms).

Axioms
------

|       Name       |                         Definition                          |
| :--------------: | :---------------------------------------------------------: |
|  Associativity   | $$\forall a,b,c\in G, (a\circ b)\circ c=a\circ (b\circ c)$$ |
|     Closure      |             $$\forall a,b\in G, a\circ b\in G$$             |
| Identity Element |    $$\exist e\in G:\forall a\in G, e\circ a=a\circ e=a$$    |
| Inverse Element  |   $$\forall a\in G, \exists b\in G:a\circ b=b\circ a=e$$    |

Underlying Set
--------------
A group $(G,\circ)$ is sometimes referred to by its _underlying set_ directly, e.g. $G$.

Morphisms
---------
Homomorphism
  ~ A map between groups that respects the group structure, i.e iff. $$\phi\colon G_1\rightarrow G_2$$ is a homomorphism then 
  $$
  \forall\,a,b\in G_1,G_2 : \phi(a\circ b) = \phi(a)\circ\phi(b)\,.
  $$
  
Isomorphism
  ~ A bijective group homomorphism, represented by $G_1\cong G_2$.

## Examples

### Abelian Groups

An Abelian Group (or commutative group) is a group in which the result of applying the group operation does not depend upon the order of the elements upon which it operates, e.g. $$a\circ b=b\circ a$$

An example of Abelian groups is the integers under addition $(\mathcal{Z},\circ +)$ as
$$1+2 = 2+1\,.$$
