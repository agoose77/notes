# Fundamental Theorem of Calculus

The fundamental theorem of calculus links the concept of differentiating a function with the concept of integrating a function.

<div style="color: #004085;background-color: #cce5ff;border-color: #b8daff;   position: relative;padding: .75rem 1.25rem;margin-bottom: 1rem;border: 1px solid transparent;border-radius: .25rem;">
    
### The Antiderivative
An _antiderivative_ of some function $f$ is the function $F$ whose derivative is equal to the original function $f$, i.e. $$F^\prime = f\,.$$
    
If $F(x)$ is _any_ antiderivative of $f(x)$, the _most general_ antiderivative is the _indefinite integral_ of $f(x)$, 
$$
    \tag{a}
    \int f(x)\,\mathrm{d}x = F(x) + c\,,
$$
where $c$ is any constant. In effect, **(a)** represents the _set of antiderivatives_ of $f(x)$.
</div>

The theorem has two parts:

## First Fundamental Theorem of Calculus

### Theorem

If $f$ is a continuous function defined on the _closed_ interval $I=[a,b]$, and $F$ is its _accumulation_ function defined by

$$
\tag{b}
F(x)=\int_a^xf(t)\,\mathrm{d}{t}\,,
$$

then $F$ is uniformly continuous on $I$, differentiable on the open interval $(a, b)$, and
$$F^\prime(x)=f(x)\,,$$

that is, _there exists an antiderivative $F(x)$ of $f(x)$ given by **(b)**_.

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

Let

$$
    \tag{c}
    G(x) = \int_a^x f(t)\,\mathrm{d}t\,.
$$

By the _first fundamental theorem of calculus_, $G$ is an antiderivative of $f$, or

$$
    G^\prime(x)=f(x)\,.
$$

As $F$ is _also_ an antiderivative of $f$, it follows that

$$
    \tag{d}
    G(x)=F(x)+C\,,
$$

such that $G$ and $F$ differ only by a constant. But using **(c\)**,

$$
\begin{aligned}
G(a) &= F(a) + C\\
     &= \int_a^a f(t)\,\mathrm{d}t = 0\,,
\end{aligned}
$$

hence $C=-F(a)$. This gives

$$
\int_a^b f(t)\,\mathrm{d}t = F(b) - F(a)\,.
$$

<!-- For subsequent "proper" derivation of rule 2, we can't define rule 1 in terms of rule 2, as rule 2 makes presupposition that _any_ antiderivative exists. This is only proven by rule 1. -->
