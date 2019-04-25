Inner Product Space
===================
An inner product space is a [vector space](vector-space.md) with an additional structure called an _inner product_, which associates pairs of vectors in the space $V$ with a scalar value in the field $F$.

## The Inner Product
<div style="padding:15px;margin-bottom:20px;border:1px solid transparent;border-radius:4px;color:#31708f;background-color:#d9edf7
;border-color:#bce8f1;">
    
### Definitions
Hermitian form
  ~ A conjugate-symmetric sesquilinear form.
    
Sesquilinear form
  ~ A bilinear form $S$ on a vector space $V$ over a field $K$, one of whose arguments behaves semilinearly, i.e. there exists some automorphism $\phi\colon K\rightarrow K$ such that for $\vb{x},\vb{y}\in V$ and $a,b\in K$
    $$
    \begin{aligned}
    S(ax, y) = aS(x, y)\\
    S(x, by) = \phi(b)S(x, y)\,.
    \end{aligned}
    $$
    
Automorphism
  ~ A bijection from some algebraic structure $K$ to itself, which *preserves the operations of addition and multiplication*.
    
Bijection
  ~ A function between the elements of two sets, where each element of one set is paired with *exactly one* element of the other set, and vice-versa.

Bilinear form
  ~ A bilinear map $V\times V\rightarrow K$ where $K$ is the field of scalars.
  <!-- The *canonical basis* B of a bilinear form T is that for which  T(ui,uj)=0 for ui, uj ∈ B -->
Bilinear map
  ~ A function $V\times W \rightarrow X$ combining elements of $V$ and $W$ to yield an element of a third vector space $X$, linear in each of its arguments, e.g. matrix multiplication.
</div>

The inner product is a *sesquilinear form*, with the automorphism $\phi\colon x\mapsto \overline{x}$:
$$
\ip{\cdot}{\cdot}\colon V\times V\rightarrow F\,,
$$
which satisfies the following three axioms $\forall\, x,y,z\in V$ and $\forall\, a\in F$:

|               Name              	|                                                   Definition                                                                 	|
|:-------------------------------:	|:-----------------------------------------------------------------------------------------------------------------------------:|
|        Conjugate Symmetry       	|                                 $\lang u,v\rang=\overline{\lang v,u\rang}$                                                   	|
| Linearity in the first argument 	| $$\begin{aligned}\lang au,v\rang&=a\lang u,v\rang\\\lang u_1+u_2,v\rang &=\lang u_1,v\rang+\lang u_2,v\rang\end{aligned}$$ 	|
| Positive-definiteness           	| $$\begin{aligned}\lang u,u\rang &\ge 0\\ &= 0 \iff u=0\end{aligned}$$       	|

More concisely, it is a *positive-definite Hermitian form*.

Vector Norm
-----------
Any inner product space has a *naturally* defined norm given by 
$$
\abs{\vb{v}} = \sqrt{\ip{\vb{v}}{\vb{v}}}\,.
$$

Basis Representation Over Complex Field
---------------------------------------
Let $\mathcal{B} = \set{\vb{b}_1,\,\vb{b}_2,\,\dots,\,\vb{u}_n}$ be a basis of an $n$-dimensional inner product space $V$. Given two vectors $\vb{u},\vb{v}\in V$, we can express them in terms of $\mathcal{B}$
$$
\begin{aligned}
    \vb{u} &= x_1\vb{b}_1 + x_2\vb{b}_2 + \dots + x_n\vb{u}_n\\
    \vb{v} &= y_1\vb{b}_1 + y_2\vb{b}_2 + \dots + y_n\vb{u}_n\,.
\end{aligned}
$$

Linearity implies
$$
\begin{aligned}
\ip{\vb{u}}{\vb{v}} &= \ip{\sum_{i=1}^nx_i\vb{b}_i}{\sum_{j=1}^ny_i\vb{b}_i}\\
                    &= \sum_{i=1}^n \sum_{j=1}^n x_i \overline{y_i}\ip{\vb{b}_i}{\vb{b}_i}\,.
\end{aligned}
$$
The terms $\ip{\vb{b}_i}{\vb{b}_i}$ correspond to elements of the *matrix of the inner product relative to the basis $\mathcal{B}$*. Thus, using coordinate vectors in $\mathcal{B}$,
$$
\begin{array}{cc}
\vb{u}_\mathcal{B} = \begin{bmatrix}x_1 & x_2 & \dots & x_n\end{bmatrix}^T, & \vb{v}_\mathcal{B} = \begin{bmatrix}y_1 & y_2 & \dots & y_n\end{bmatrix}^T\,,
\end{array}
$$
we have 
$$
\tag{a}
\ip{\vb{u}}{\vb{v}} = \vb{u}_\mathcal{B}^TA_\mathcal{B}\overline{\vb{v}_\mathcal{B}}\,,
$$
where 
$$
\def\el#1#2{\ip{\vb{b}_#1}{\vb{b}_#2}}
A_\mathcal{B} = \begin{bmatrix} 
    \el{1}{1} & \el{1}{2} & \dots  & \el{1}{n} \\
    \el{2}{1} & \el{2}{2} & \dots  & \el{2}{n} \\
    \vdots    & \vdots    & \ddots & \vdots    \\
    \el{n}{1} & \el{n}{2} & \dots  & \el{n}{n}
\end{bmatrix}
$$ 
must be positive definite to satisfy *positive-definiteness* of the general inner product. As $A_\mathcal{B}$ is formed of inner products, which posses conjugate symmetry, it follows that $A_\mathcal{B}^\dagger = A_\mathcal{B}$, and hence $A$ is Hermitian[^1]. The matrix $A_{ij}=\ip{\vb{b}_i}{\vb{b}_j}$ is the [Gram matrix](https://en.wikipedia.org/wiki/Gramian_matrix) of the basis vectors $\set{\vb{b}_i}$.
Note that, as a scalar, the inner product is invariant under transposition, thus we may rewrite **(a)** as 
$$
\begin{aligned}
\ip{\vb{u}}{\vb{v}} &= \left(\vb{u}_\mathcal{B}^TA_\mathcal{B}\overline{\vb{v}_\mathcal{B}}\right)^T\\
                    &= \vb{v}_\mathcal{B}^\dagger \left(\vb{u}_\mathcal{B}^TA_\mathcal{B}\right)^T\\
                    &= \vb{v}_\mathcal{B}^\dagger A_\mathcal{B}^T\vb{u}_\mathcal{B}\\
\end{aligned}
$$
<!-- N.B. basis vectors do not need to be orthonormal, only linearly independent, and span the space -->

[^1]: [Square Matrices](square-matrices.md#Hermitian-%5BNormal%5D)