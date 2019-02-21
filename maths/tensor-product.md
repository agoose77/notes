# Tensor Product
The tensor product $V\otimes W$ of two [vector spaces](vector-space.md) $V$ and $W$ over the same field is also a vector space. 

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
Given that $\otimes$ is linear in both arguments, if $V$ has basis $\{\vec{p}_i\}$, and $W$ has basis $\{\vec{q}_i\}$, then for $v\in V,w\in W$:

$$
\begin{aligned}
v\otimes w &= \sum_iv_i\vec{p}_i\otimes\sum_i w_i\vec{q}_i \\
           &= \sum_iv_i\left(\vec{p}_i\otimes\sum_i w_i\vec{q}_i\right) \\
           &= \sum_i \sum_j v_i w_j \left(\vec{p}_i\otimes \vec{q}_j\right)\,,
\end{aligned}
$$
which shows that $\{p_i\otimes q_j\}$ is a basis of $V\otimes W$.

## Tensor Product of Linear Maps
Given two linear maps $S:V\rightarrow A$ and $T:W\rightarrow B$, the tensor product of $S,T$ is also a linear map, defined by 
$$
(S\otimes T)(v\otimes w)=S(v)\otimes T(w)\,.
$$

Elements of $V\otimes W$ can be operated upon by $S,T$ individually, though the identity element:
$$
\begin{aligned}
(S\otimes 1_T)(v\otimes w) &= (Sv)\otimes w\\
(1_S\otimes T)(v\otimes w) &= v\otimes (Tw)\\
\end{aligned}
$$