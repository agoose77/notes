# Linear Adjoint

Let $V$ and $W$ be finite-dimensional [inner product spaces](inner-product-space.md) over the same [field](../field.md) $F$, and let $T$ be a linear map i.e. $T\in\mathcal{L}(V,W)$, where $\mathcal{L}(V,W)$ is the [vector space](vector-space.md) of all [linear maps](linear-mapping.md) from $V$ to $W$. A function $T^*\colon W\rightarrow V$ is called an _adjoint_ of $T$ if

$$
\ip{T(\vb{v})}{\vb{w}} = \ip{\vb{v}}{T^*(\vb{w})}\,\forall\,\vb{v}\in V,\vb{w}\in W\,.
$$

## Proof[^1]

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

Thus it is shown that $T^*$ is a _linear map_ from $W$ to $V$, i.e. $T^* \in \mathcal{L}(W,V)$.

## Inner Product

The adjoint is defined in terms of the inner product. In matrix form, it must be defined in terms of a particular basis, as the inner product itself depends upon the basis

$$
\ip{\vb{u}}{\vb{v}} = \vb{v}_\mathcal{B}^\dagger H_\mathcal{B}\vb{u}_\mathcal{B}\,.
$$

Without the basis subscript, **(a)** is written

$$
\vb{y}^\dagger H_WT\vb{x} = \vb{y}^\dagger {T^*}^\dagger H_V\vb{x}\,,
$$

which yields the definition of the adjoint $T^*$[^2]:

$$
\begin{aligned}
H_WT &= {T^*}^\dagger H_V\\
H_W T H_V^{-1} &= {T^*}^\dagger\\
H_W^{-1} T^\dagger H_V &= T^*\,.
\end{aligned}
$$

Hence, for _orthonormal_ bases $V$ and $W$, it holds that $T^* = T^\dagger$[^3][^4][^5].
From Shilov[^6]

> [E]very operator A with a Hermitian-
> symmetric matrix (i.e., a matrix equal to its own Hermitian conjugate) in
> some orthonormal basis is self-adjoint.

<!-- Note that BY DEFINITION the matrix form of an operator assumes some fixed basis B. Unlike the linear operator it represents, this information is fundamental to its definition 

[^1]: https://people.math.osu.edu/costin.10/5101/Orthog%20p6-12.pdf
[^2]: https://math.stackexchange.com/a/1320924
[^3]: http://math.stanford.edu/~akshay/math113/11.12.pdf
[^4]: Linear Algebra, Werner Greub (auth.), p.217
[^5]: https://math.stackexchange.com/questions/2362774/relationship-between-definition-of-adjoint-of-a-linear-operator-and-the-transpos
[^6]: Linear Algebra, Shilov, p.262
