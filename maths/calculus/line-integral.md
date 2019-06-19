Line Integral
=============
Scalar Field
------------

For some scalar [field](../field.md) $f\colon U\subseteq \mathbb{R}^n\rightarrow \mathbb{R}$, the line integral along a [piecewise smooth curve](../piecewise-functions.ipynb) $\gamma\subset U$ is defined as
$$
\int\limits_\gamma f(\vb{r})\dd{s} = \int_a^bf(\vb{r}(t))\abs{\vb{r}'(t)}\dd{t}\,,
$$
where $\vb{r}\colon [a,b]\rightarrow\gamma$ is an arbitrary [bijective](https://en.wikipedia.org/wiki/Bijection) parametrization such that $\vb{r}(a)$ and $\vb{r}(b)$ give the endpoints of $\gamma$, with $b > a$. Under the integral, $\dd{s}$ may be interpreted as the elementary arc length.

The line integral over a scalar field $f$ may be considered as the area under the curve along a surface $z=f(x, y)$.
![Line integral of scalar field](https://upload.wikimedia.org/wikipedia/commons/4/42/Line_integral_of_scalar_field.gif)

### Derivation
By approximating the curve $\gamma$ to a polygonal path, we have
$$
I=\lim_{\Delta s_i\rightarrow 0}\sum_{i=1}^nf(\vb{r}(t_i))\Delta s_i
$$

<div style="color: #004085;background-color: #cce5ff;border-color: #b8daff;   position: relative;padding: .75rem 1.25rem;margin-bottom: 1rem;border: 1px solid transparent;border-radius: .25rem;">
    
### Mean Value Theorem
The mean value theorem states that for a function $f(x)$ that is continuous on $[a,b]$ and differentiable on $(a,b)$[^open-ended], there exists some $c\in(a,b)$ for which
$$
f'(c) = \frac{f(b)-f(a)}{b-a} \,.
$$
    
![](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ee/Mvt2.svg/260px-Mvt2.svg.png)
    
</div>

From the mean value theorem we have
$$
\Delta s_i = \abs{\vb{r}(t_i+\Delta t)-\vb{r}(t_i)}\approx\abs{\vb{r}'(t_i^*)}\Delta t\,,
$$
where $t_i^*\in[t_i,t_i+\Delta t]$
and hence $I$ becomes
$$
I=\lim_{\Delta t\rightarrow 0}\sum_{i=1}^nf(\vb{r}(t_i))\abs{\vb{r}'(t_i^*)}\Delta t\,,
$$
which is a Riemmann sum for the integral
$$
I=\int_a^b f(\vb{r}(t))\abs{\vb{r}'(t)}\dd{t}\,.
$$


Vector Field
------------
For a vector field $F\colon U\subseteq \mathbb{R}^n\rightarrow\mathbb{R}^n$, the line integral along a piecewise smooth curve $\gamma\subset U$, in the direction of $\vb{r}$, is defined as
$$
\int\limits_\gamma\vb{F}(\vb{r})\cdot\dd{r} = \int_a^b\vb{F}(\vb{r}(t))\cdot\vb{r}'(t)\dd{t}\,.
$$

![Line integral of vector field.](https://upload.wikimedia.org/wikipedia/commons/b/b0/Line_integral_of_vector_field.gif)

### Derivation
By approximating the curve $\gamma$ to a polygonal path as above, we have
$$
I=\lim_{\abs{\Delta \vb{r}_i}\rightarrow 0}\sum_{i=1}^nf(\vb{r}(t_i))\cdot\Delta\vb{r}_i
$$

From the mean value theorem we have
$$
\Delta \vb{r}_i = \vb{r}(t_i+\Delta t)-\vb{r}(t_i)\approx\vb{r}'(t_i^*)\Delta t\,,
$$
where $t_i^*\in[t_i,t_i+\Delta t]$
and hence $I$ becomes
$$
I=\lim_{\Delta t\rightarrow 0}\sum_{i=1}^nf(\vb{r}(t_i))\cdot\vb{r}'(t_i^*)\Delta t\,,
$$
which is a Riemmann sum for the integral
$$
I=\int_a^b f(\vb{r}(t))\cdot\vb{r}'(t)\dd{t}\,.
$$


[^open-ended]: The derivative depends on the existence of the two-sided [limit](../limit.md). At the endpoints of an interval, the derivative is therefore not defined (though the one-sided derivative is).