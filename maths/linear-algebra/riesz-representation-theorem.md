Riesz Representation Theorem
============================  
For all [linear functionals](linear-mapping.md#Linear-Functional) $\phi\in V^*\colon V\rightarrow F$ on a finite-dimensional vector space $V$ there exists a unique vector $\vb{v}\in V$ such that $\phi(\vb{u})=\ip{\vb{u}}{\vb{v}}$ for $\vb{u}\in V$.[^1]
  
Proof

---

Let $\set{\vu{e}_1,\,\vu{e}_2,\,\dots,\,\vu{e}_n}$ be an orthonormal basis of $V$. It can be shown via the Gram-Schmidt process that every finite-dimensional inner product space has an orthonormal basis.

<!-- TODO Gram Schmidt -->

Any vector $\vb{u}\in V$ may written in terms of this basis,

$$
    \vb{u} = \sum_iu_i\vu{e}_i\,.
$$

From the definition of the inner product,

$$
\begin{aligned}
\ip{\vb{u}}{\vu{e}_j} &= \ip{\sum_iu_i\vu{e}_i}{\vu{e}_j} \\
                      &= \sum_iu_i\ip{\vu{e}_i}{\vu{e}_j}\\
                      &= u_j\,,
\end{aligned}
$$

hence $\vb{u}$ may be expanded in terms of the inner product on $V$:

$$
    \vb{u} = \sum_i\ip{\vb{u}}{\vu{e}_i}\vu{e}_i\,.
$$

Since $\phi(\vb{u})$ is a linear functional, we have that

$$
\begin{aligned}
\phi(\vb{u}) &= \phi\mleftright{(}{\ip{\vb{u}}{\vu{e}_1}\vu{e}_1 + \ip{\vb{u}}{\vu{e}_2}\vu{e}_2 + \dots + \ip{\vb{u}}{\vu{e}_n}\vu{e}_n}{)}\\
&= \ip{\vb{u}}{\vu{e}_1}\phi(\vu{e}_1) + \ip{\vb{u}}{\vu{e}_2}\phi(\vu{e}_2) + \dots + \ip{\vb{u}}{\vu{e}_n}\phi(\vu{e}_n)\\
&= \ip{\vb{u}}{\overline{\phi(\vu{e}_1)}\vu{e}_1} + \ip{\vb{u}}{\overline{\phi(\vu{e}_2)}\vu{e}_2} + \dots + \ip{\vb{u}}{\overline{\phi(\vu{e}_n)}\vu{e}_n}\\
\end{aligned}
$$

Let $
\vb{v} = \overline{\phi(\vu{e}_1)}\vu{e}_1 + \overline{\phi(\vu{e}_2)}\vu{e}_2 + \dots + \overline{\phi(\vu{e}_n)}\vu{e}_n
$, then for every $\vb{u}\in V$ we have that $\phi(\vb{u}) = \ip{\vb{u}}{\vb{v}}$. It must now be shown that $\vb{v}$ is unique. Suppose that there exist two vectors $\vb{v},\vb{v'}\in V$ such that $\phi(\vb{u}) = \ip{\vb{u}}{\vb{v}}=\ip{\vb{u}}{\vb{v'}}$. Then, for every $\vb{u}\in V$

$$
\begin{aligned}
0 &= \ip{\vb{u}}{\vb{v}} - \ip{\vb{u}}{\vb{v'}}\\
&= \ip{\vb{u}}{\vb{v} - \vb{v'}}\,.
\end{aligned}
$$

Given that we defined $\vb{v}$ and $\vb{v'}$ independently of $\vb{u}$, it follows that if we take $\vb{u}=\vb{v}-\vb{v'}$,

$$
\ip{\vb{v} - \vb{v'}}{\vb{v} - \vb{v'}} = 0\,,
$$

which given _positive-definiteness_ of $\ip{\cdot}{\cdot}$ holds iff. $\vb{v}-\vb{v'}=\vb{0}$.
  
Thus, we have $\phi(\vb{u}) = \ip{\vb{u}}{\vb{v}}$ for a _unique_ $\vb{v}$. $\qed$

[^1]: http://mathonline.wikidot.com/linear-functionals
