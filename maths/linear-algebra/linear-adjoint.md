Linear Adjoint
==============
Let $V$ and $W$ be finite-dimensional [inner product spaces](inner-product-space.md) over the same [field](../field.md) $F$, and let $T$ be a linear map i.e. $T\in\mathcal{L}(V,W)$, where $\mathcal{L}(V,W)$ is the [vector space](vector-space.md) of all [linear maps](linear-mapping.md) from $V$ to $W$. A function $T^*\colon W\rightarrow V$ is called an *adjoint* of $T$ if
$$
\ip{T(\vb{v})}{\vb{w}} = \ip{\vb{v}}{T^*(\vb{w})}\,\forall\,\vb{v}\in V,\vb{w}\in W\,.
$$

Proof[^1]
---------
For every fixed $\vb{y}\in W$, let us define a linearly functional $\phi(\vb{x})=\ip{T(\vb{x})}{\vb{y}}$ for $\vb{x}\in V$. By the [Riesz representation theorem](riesz-representation-theorem.md), there exists a unique vector $\vb{z}\in W$ such that $\phi(\vb{x})$ may be written in the form $\phi(\vb{x})=\ip{\vb{x}}{\vb{z}}$, i.e.
$$
\ip{T(\vb{x})}{\vb{y}} = \ip{\vb{x}}{\vb{z}}\,.
$$
Hence, let us define $T^*(\vb{y})=\vb{z}$ such that
$$
\tag{a}
\ip{T(\vb{x})}{\vb{y}} = \ip{\vb{x}}{T^*(\vb{y})}\,.
$$


Let $\vb{w}_1,\vb{w}_2\in W$ and $a,b\in F$. It follows that
$$
\begin{aligned}
\ip{T(\vb{v})}{a\vb{w}_1 + b\vb{w}_2} &= \ip{T(\vb{v})}{a\vb{w}_1}+\ip{T(\vb{v})}{b\vb{w}_2}\\
&= \overline{a}\ip{T(\vb{v})}{\vb{w}_1}+\overline{b}\ip{T(\vb{v})}{\vb{w}_2}\\
&= \overline{a}\ip{\vb{v}}{T^*(\vb{w}_1)+\overline{b}\ip{\vb{v}}{T^*(\vb{w}_2)}}\\
&= \ip{\vb{v}}{aT^*(\vb{w}_1)+\ip{\vb{v}}{bT^*(\vb{w}_2)}}\\
&= \ip{\vb{v}}{T^*(a\vb{w}_1+b\vb{w}_2)}\,.
\end{aligned}
$$
Thus it is shown that $T^*$ is a *linear map* from $W$ to $V$, i.e. $T^* \in \mathcal{L}(W,V)$. 

Inner Product
-------------
The adjoint is defined in terms of the inner product. Consequently, in matrix form, the adjoint can only be defined in terms of a particular basis, as the inner product itself depends upon the basis
$$
\ip{\vb{u}}{\vb{v}} = \vb{u}_\mathcal{B}^T A_\mathcal{B}\overline{\vb{v}_\mathcal{B}}\,.
$$
Without the basis subscript, in matrix form, Eq. **(a)** is written
$$
\vb{x}^TT^T A\overline{\vb{y}} = \vb{x}^T A\overline{T^*}\overline{\vb{y}}\,,
$$
which yields the definition of the adjoint $T^*$:
$$
\begin{aligned}
T^TA &= A\overline{T^*}\\
\overline{A^{-1}}T^\dagger\overline{A} &= T^*\\
\overline{A}^{-1}T^\dagger\overline{A} &= T^*\,.
\end{aligned}
$$

[^1]: https://people.math.osu.edu/costin.10/5101/Orthog%20p6-12.pdf