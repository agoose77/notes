Inner Product Space
===================
An inner product space is a [vector space](vector-space.md) with an additional structure called an _inner product_, which associates pairs of vectors in the space $V$ with a scalar value in the field $F$.

## The Inner Product
The inner product is a map:
$$
\lang \cdot,\cdot\rang\colon V\times V\rightarrow F\,,
$$
which satisfies the following three axioms $\forall\, x,y,z\in V$ and $\forall\, a\in F$:

|               Name              	|                                                   Definition                                                  	|
|:-------------------------------:	|:-------------------------------------------------------------------------------------------------------------:	|
|        Conjugate Symmetry       	|                                 $\lang u,v\rang=\overline{\lang v,u\rang}$                                	|
| Linearity in the first argument 	| $$\begin{aligned}\lang au,v\rang&=a\lang u,v\rang\\
\lang u_1+u_2,v\rang &=\lang u_1,v\rang+\lang u_2,v\rang\end{aligned}$$ 	|
| Positive-definiteness           	| $$\begin{aligned}\lang u,u\rang &\ge 0\\ &= 0 \iff u=0\end{aligned}$$                                      	|