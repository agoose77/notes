# Vector Spaces
A vector space over a field $F$ is a set $V$, together with two operations which satisfy a series of [axioms](#Axioms). Elements of $V$ are called _vectors_, whilst elements of $F$ are called _scalars_.

## Operations
|          Name         	|         Definition         	|
|:---------------------:	|:--------------------------:	|
|    Vector Addition    	| $+:V\times V\rightarrow V$ 	|
| Scalar Multiplication 	| $+:F\times V\rightarrow V$ 	|

For both operations, the result is also a member of $V$.

## Axioms

|  Name                                                            	| Definition                                      	|
|------------------------------------------------------------------	|-------------------------------------------------	|
| Associativity of addition                                        	| $u + (v + w) = (u + v) + w$                     	|
| Commutativity of addition                                        	| $u + v = v + u$                                 	|
| Identity element of addition                                     	| $\exist 0\in V: \forall v\in V, v + 0 = v $     	|
| Inverse elements of addition                                     	| $\forall v\in V,\exists -v\in V : v + (-v) = 0$ 	|
| Compatibility of scalar multiplication with field multiplication 	| $a(bv) = (ab)v$                                 	|
| Identity element of scalar multiplication                        	| $1v = v$                                        	|
| Distributivity of scalar multiplication w.r.t vector addition    	| $a(u + v) = au + av$                            	|
| Distributivity of scalar multiplication w.r.t field addition     	| $(a + b)v = av + bv$                            	|

This first four of these axioms are equivalent to defining vectors as _an [abelian group](groups.md/#Abelian-Groups) under addition_.