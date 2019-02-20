# Inner Product Space
An inner product space is a [vector space](vector-space.md) with an additional structure called an _inner product_, which associates pairs of vectors in the space $V$ with a scalar value in the field $F$.

## The Inner Product
The inner product is a map:
$$
\left<\cdot,\cdot\right>:V\times V\rightarrow F\,
$$
which satisfies the following three axioms $\forall x,y,z\in V$ and $\forall a\in F$:

|               Name              	|                                                   Definition                                                  	|
|:-------------------------------:	|:-------------------------------------------------------------------------------------------------------------:	|
|        Conjugate Symmetry       	|                                 $\left<u,v\right>=\overline{\left<v,u\right>}$                                	|
| Linearity in the first argument 	| $$\begin{aligned}\left<au,v\right>&=a\left<u,v\right>\\
\left<u_1+u_2,v\right> &=\left<u_1,v\right>+\left<u_2,v\right>\end{aligned}$$ 	|
| Positive-definiteness           	| $$\begin{aligned}\left<u,u\right> &\ge 0\\ &= 0 \iff u=0\end{aligned}$$                                      	|