Vector space-subspace proof
============================
Let $A=\{\,\vec{a_1},\,\vec{a_2},\,\dots,\,\vec{a_n}\,\}$ be a basis of a vector space $V$.

It can be shown that _any_ [spanning](vector-space.md#Basis-and-Dimension) [set](../set.md) must have _at least_ $n$ elements.

Proof
-----
Let $$B=\{\,\vec{b_1},\,\vec{b_2},\,\dots,\,\vec{b_m}\,\}$$ span $V$, where $m<n$. We can then define $B_1'=\{\,\vec{a_1},\,\vec{b_2},\,\dots,\,\vec{b_m}\,\}$, which will be linearly dependent (as $\vec{a_1}$ can be formed from $B$'s span). After removing $\vec{b_i}:i=1,\dots,n$, we can then define $$B_1=\{\,\vec{a_1},\,\vec{b_2},\,\dots,\,\vec{b_m}\,\}\,,$$ which restores linear independence. This process can be repeated $m-1$ times until we are left with $B_m$, which spans $V$ (as $B$ spans $V$). As $B_m$ spans $V$, and is a subset of $A$, it follows that $A$ is _not_ linearly independent, and hence cannot be a basis of $V$. Thus, any spanning set of $V$ must have _at least_ $n$ elements.