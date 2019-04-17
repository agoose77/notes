Inner Product Space
===================
An inner product space is a [vector space](vector-space.md) with an additional structure called an _inner product_, which associates pairs of vectors in the space $V$ with a scalar value in the field $F$.

## The Inner Product
<div style="padding:15px;margin-bottom:20px;border:1px solid transparent;border-radius:4px;color:#31708f;background-color:#d9edf7
;border-color:#bce8f1;">
        
#### Sesquilinear Forms etc.
A *sesquilinear form* $\alpha$ on a vector space $V$ over a field $K$ is a bilinear form on $V$, one of whose arguments behaves semilinearly, i.e. there exists some automorphism $\phi\colon K\rightarrow K$ such that 
    $$
    \begin{aligned}
    \alpha(ax, y) = a\alpha(x, y)\\
    \alpha(x, by) = \phi(b)\alpha(x, y)\,.
    \end{aligned}
    $$
An *automorphism* of $K$ is a bijection from $K$ to itself, which *preserves the operations of addition and multiplication*.

A *bijection* is a function between the elements of two sets, where each element of one set is paired with *exactly one* element of the other set, and vice-versa.
    
    
A *bilinear form* on a vector space $V$ is a bilinear map $V\times V\rightarrow K$ where $K$ is the field of scalars.

A *bilinear map* on vector spaces $V$ and $W$ is a function $B\colon V\times W \rightarrow X$ combining elements of $V$ and $W$ to yield an element of a third vector space $X$, and is linear in each of its arguments, e.g. matrix multiplication.
</div>
The inner product is a *sesquilinear form*, with the automorphism $\phi\colon x\mapsto \overl$:
$$
\ip{\cdot}{\cdot}\colon V\times V\rightarrow F\,,
$$
which satisfies the following three axioms $\forall\, x,y,z\in V$ and $\forall\, a\in F$:

|               Name              	|                                                   Definition                                                                 	|
|:-------------------------------:	|:-----------------------------------------------------------------------------------------------------------------------------:|
|        Conjugate Symmetry       	|                                 $\lang u,v\rang=\overline{\lang v,u\rang}$                                                   	|
| Linearity in the first argument 	| $$\begin{aligned}\lang au,v\rang&=a\lang u,v\rang\\\lang u_1+u_2,v\rang &=\lang u_1,v\rang+\lang u_2,v\rang\end{aligned}$$ 	|
| Positive-definiteness           	| $$\begin{aligned}\lang u,u\rang &\ge 0\\ &= 0 \iff u=0\end{aligned}$$       	|

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
\ip{\vb{u}}{\vb{v}} = \vb{u}_\mathcal{B}^TA\overline{\vb{v}_\mathcal{B}}\,,
$$
where 
$$
\def\el#1#2{\ip{\vb{b}_#1}{\vb{b}_#2}}
A = \begin{bmatrix} 
    \el{1}{1} & \el{1}{2} & \dots  & \el{1}{n} \\
    \el{2}{1} & \el{2}{2} & \dots  & \el{2}{n} \\
    \vdots    & \vdots    & \ddots & \vdots    \\
    \el{n}{1} & \el{n}{2} & \dots  & \el{n}{n}
\end{bmatrix}\,.
$$
<!-- N.B. basis vectors do not need to be orthonormal, only linearly independent, and span the space -->