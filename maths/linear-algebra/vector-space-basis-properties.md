# Vector Space Basis Properties

## Spanning Sets Have At Least $\dim(\text{Basis})$ Elements

Let $A=\{\,\vec{a_1},\,\vec{a_2},\,\dots,\,\vec{a_n}\,\}$ be a basis of a vector space $V$.

It can be shown that _any_ [spanning](vector-space.md#Basis-and-Dimension) [set](../set.md) must have _at least_ $n$ elements.

### Proof

Let $$B=\{\,\vec{b_1},\,\vec{b_2},\,\dots,\,\vec{b_m}\,\}$$ span $V$, where $m<n$. We can then define $B_1'=\{\,\vec{a_1},\,\vec{b_2},\,\dots,\,\vec{b_m}\,\}$, which will be linearly dependent (as $\vec{a_1}$ can be formed from $B$'s span). After removing $\vec{b_i}:i=1,\dots,n$, we can then define $$B_1=\{\,\vec{a_1},\,\vec{b_2},\,\dots,\,\vec{b_m}\,\}\,,$$ which restores linear independence. This process can be repeated $m-1$ times until we are left with $B_m$, which spans $V$ (as $B$ spans $V$). As $B_m$ spans $V$, and is a subset of $A$, it follows that $A$ is _not_ linearly independent, and hence cannot be a basis of $V$. Thus, any spanning set of $V$ must have _at least_ $n$ elements.

## Bases Have Same Dimension

Consider two sets of vectors, $B=\set{\vb{v}_1,\,\vb{v}_2,\,\dots,\,\vb{v}_n}$ and $B'=\set{\vb{w}_1,\,\vb{w}_2,\,\dots,\,\vb{w}_m}$, where $\vb{v},\vb{w}\in V$ for some vector space $V$.

In order for both $B$ and $B'$ to be bases of $V$, $n$ must equal $m$.

### Proof

If we take one basis as $B$, it follows that the set of linearly independent (as a basis) vectors $B'$ must have _at most_ $n$ elements (or else they would not be linearly independent). Similarly, considering $B'$ as a basis, $B$ must have _at most_ $m$ elements. These two relations

$$
\begin{matrix}
n \leq m\,, & m \leq n\,,
\end{matrix}
$$

are only satisfed if $n = m$, hence all bases of a vector space must have the same number of elements.
