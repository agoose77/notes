Conservative Vector Field
=========================
A conservative vector field (gradient field) is a [vector field](https://en.wikipedia.org/wiki/Vector_field) that is the gradient of some function.

That is, a vector field $\vb{v}\colon U\rightarrow\mathbb{R}^n$ is said to be conservative iff. there exists a scalar field $\phi\colon U\rightarrow \mathbb{R}$ such that
$$
\vb{v}=\nabla \phi\,,
$$
where $U\subseteq \mathbb{R}^n$.
When the above holds, $\phi$ is the *scalar potential* of $\vb{v}$.

Properties
----------
1. $\int\limits_\vb{\gamma}\vb{v}\cdot\dd{\vb{r}}=\phi(\vb{q})-\phi(\vb{p})$ where $\vb{p},\vb{q}\in U$ are the endpoints of the path $\vb{\gamma}$. This result is known as the *gradient theorem*. It is proven as follows:  
    From the [multivariate chain rule](calculus/total-derivative.md), we have for $\vb{r}(t)\colon \mathbb{R}\rightarrow U$ differentiable on $[a,b]$
    $$
    \dv{}{t}\left(\comp{\phi}{\vb{r}}\right)(t) = \nabla\phi\mleftright{(}{\vb{r}(t)}{)}\cdot\vb{r}'(t)\,,
    $$
    for all $t\in(a,b)$.

    $$
    \begin{aligned}
    \int\limits_\vb{\gamma}\vb{v}\cdot\dd{\vb{r}} 
    &= \int\limits_\vb{\gamma}\nabla \phi\cdot\dd{\vb{r}}\\
    &= \int_a^b\dv{}{t}\phi(\vb{r}(t))\dd t
    \end{aligned}
    $$
    From the [second fundamental theorem of calculus](calculus/fundamental-theorem-of-calculus.md), we have
    $$
    \int\limits_\vb{\gamma}\vb{v}\cdot\dd{\vb{r}} = \phi(\vb{r}(b)) - \phi(\vb{r}(a)) = \phi(\vb{q}) - \phi(\vb{p})\,.
    $$