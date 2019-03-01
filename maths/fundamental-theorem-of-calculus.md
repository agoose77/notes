# Fundamental Theorem of Calculus
The fundamental theorem of calculus links the concept of differentiating a function with the concept of integrating a function.
 
<div style="color: #004085;background-color: #cce5ff;border-color: #b8daff;   position: relative;padding: .75rem 1.25rem;margin-bottom: 1rem;border: 1px solid transparent;border-radius: .25rem;">
    
### The Antiderivative
The _antiderivative_ of some function $f$ is the function $F$ whose derivative is equal to the original function $f$, i.e. $$F^\prime = f\,.$$
    
If $F(x)$ is _any_ antiderivative of $f(x)$, the _most general_ antiderivative is the _indefinite integral_ of $f(x)$, 
$$
    \int f(x)\,\mathrm{d}x = F(x) + c\,,
$$
where $c$ is any constant.
</div>

The theorem has two parts:

## First Fundamental Theorem of Calculus
### Theorem
If $f$ is a continuous function defined on the _closed_ interval $I=[a,b]$, and $F$ is its _accumulation_ function defined by
$$
\tag{a}
F(x)=\int_a^xf(t)\,\mathrm{d}{t}\,,
$$
then $F$ is uniformly continuous on $I$, differentiable on the open interval $(a, b)$, and
$$F^\prime(x)=f(x)\,,$$

that is, _there exists an antiderivative $F(x)$ of $f(x)$ given by **(a)**_.
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

<div style="color: #004085;background-color: #cce5ff;border-color: #b8daff;   position: relative;padding: .75rem 1.25rem;margin-bottom: 1rem;border: 1px solid transparent;border-radius: .25rem;">

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
If $F$ is an _antiderivative_ of $f$, with $f$ a continuous function defined on the _closed_ interval $I=[a,b]$, then
$$
\int_a^b f(x)\,\mathrm{d}x=F(b)-F(a)\,.
$$

It also holds from [the first fundamental theorem of calculus](#First-Fundamental-Theorem-of-Calculus) that if $f$ is continuous, then there exists an antiderivative.
<div style="color: #856404;background-color: #fff3cd;border-color: #ffeeba;position: relative;padding: .75rem 1.25rem;margin-bottom: 1rem;border: 1px solid transparent;border-radius: .25rem;">
Note, this is a weaker form of the proof (requiring continuity of $f$). A stronger proof makes use of Riemann sums.
</div>

### Proof
Let $$G(x) = \int_a^xF^\prime(t)\,\mathrm{d}t\,.$$

By the _first fundamental theorem of calculus_, $G^\prime(x)=F^\prime(x)$, hence $G(x)=F(x)+C$. 

But, 
$$
G(a)=\int_a^a F^\prime(t)\,\mathrm{d}t=0\,,
$$
and $G(a)=F(a)+C$, so $C=-F(a)$. 

This gives
$$
\int_a^bF^\prime(t)\,\mathrm{d}t = F(b) - F(a)\,.
$$

<!-- For subsequent "proper" derivation of rule 2, we can't define rule 1 in terms of rule 2, as rule 2 makes presupposition that _any_ antiderivative exists. This is only proven by rule 1.