# Fundamental Theorem of Calculus
The fundamental theorem of calculus links the concept of differentiating a function with the concept of integrating a function. It has two parts:

## First Fundamental Theorem of Calculus
### Theorem
If $f$ is a continuous function defined on the _closed_ interval $I=[a,b]$, and $F$ is its _accumulation_ function defined by
$$
F(x)=\int_a^xf(t)\,\mathrm{d}{t}\,,
$$
then $F$ is uniformly continuous on $I$, differentiable on the open interval $(a, b)$, and
$$F^\prime(x)=f(x)\,.$$

### Proof
Let 
$$
    \Delta F = F(x+\Delta x) - F(x) = \int_a^{x+\Delta x}f(t)\,\mathrm{d}t-\int_a^xf(t)\,\mathrm{d}t\,.
$$
From the additive property of the definite integral,
$$
\begin{aligned}
    \Delta F &= \int_a^xf(t)\,\mathrm{d}t+\int_x^{x+\Delta x}f(t)\,\mathrm{d}t-\int_a^xf(t)\,\mathrm{d}t \\
             &= \int_x^{x+\Delta x}f(t)\,\mathrm{d}t\,.
\end{aligned}
$$

<div style="padding:15px;margin-bottom:20px;border:1px solid transparent;border-radius:4px;color:#31708f;background-color:#d9edf7;border-color:#bce8f1;">

#### Extreme Value Theorem
If $g(x)$ is continuous on $[a, b]$ then there exists $c,d\in[a,b]$ such that
$$g(c)\ge g(x)\ge g(d)\,,$$
for all $x\in[a,b]$.
</div>

From the _Extreme Value Theorem_, $f(x)$ in the interval $[x,x+\Delta x]$ satisfies $m_{\Delta x} \le f(x) \le M_{\Delta x}$, hence:
$$
    \int_x^{x+\Delta x}m_{\Delta x}\,\mathrm{d}t\le \int_x^{x+\Delta x}f(t)\,\mathrm{d}t\le \int_x^{x+\Delta x}M_{\Delta x}\,\mathrm{d}t\,.
$$

This reduces to
$$
    m_{\Delta x}\le \frac{1}{\Delta x}\int_x^{x+\Delta x}f(t)\,\mathrm{d}t\le M_{\Delta x}\,.
$$

As $f(x)$ is continuous, as $\Delta x\rightarrow 0$, all values of $f$ on $[x, x+\Delta x]$ approach $f(x)$, _including_ $m_{\Delta x}$ and $M_{\Delta x}$. 

Therefore,
$$
\lim_{\Delta x\rightarrow 0}\frac{1}{\Delta x}\int_x^{x+\Delta x}f(t)\,\mathrm{d}t=f(x)\,,
$$

and hence $F^\prime(x)=f(x)$.

## Second Fundamental Theorem of Calculus
### Theorem
If $F^\prime$ is a continuous function defined on the _closed_ interval $I=[a,b]$, then
$$
\int_a^b F^\prime(x)\,\mathrm{d}x=F(b)-F(a)\,.
$$

### Proof
Let $$G(x) = \int_a^xF^\prime(t)\,\mathrm{d}t\,.$$

By the _First Fundamental Theorem of Calculus_, $G^\prime(x)=F^\prime(x)$, hence $G(x)=F(x)+C$. But, 
$$
G(a)=\int_a^a F^\prime(t)\,\mathrm{d}t=0\,,
$$
and $G(a)=F(a)+C$, so $C=-F(a)$. This gives
$$
\int_a^bF^\prime(t)\,\mathrm{d}t = F(b) - F(a)
$$