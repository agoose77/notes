# Tensor Product
The tensor product $V\otimes W$ of two [vector spaces](vector-spaces.md) $V$ and $W$ over the same field is also a vector space. 

## The Operator
The tensor product operation $\otimes$ is a bilinear map, a function combining elements of two vector spaces to yield an element of a third vector space. Let $V,W,X$ be vector spaces over the same field $F$. Then $\otimes$ is defined as:
$$
\otimes: V\times W \rightarrow X
$$

As a bilinear map, $\otimes$ is linear in its arguments:
* $(v_1 + v_2)\otimes w=v_1\otimes w+v_2\otimes w$
* $v\otimes (w_1+w_2)=v\otimes w_1+v\otimes w_2$
* $(cv)\otimes w=c(v\otimes w)=v\otimes(cw)$

## The Range of $V\otimes W$
The tensor product maps from ordered pairs in the cartesian product $V\times W$ onto the space $V\otimes W$, which is generated from the set given by the tensor product of members of $V$ and $W$:
$$
X = \{v\otimes w: v\in V, w\in W\}
$$

Hence $\operatorname{dim}\left(V\otimes W\right) = \operatorname{dim}V \times \operatorname{dim}W$

## The Basis of $V\otimes W$
Given that $\otimes$ is linear in both arguments, 