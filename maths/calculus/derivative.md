Derivative
==========

Single Variable
---------------
The single variable derivative at $a$ of a real valued function $\phi\colon \mathbb{R}\rightarrow\mathbb{R}$ is defined as
$$
\tag{1}
\dv{\phi}{x}(a) = \lim_{t\rightarrow 0}\frac{\phi(a+t)-\phi(a)}{t}\,,
$$
provided that the [limit](../limit.md) exists, in which case $\phi$ is *differentiable* at $a$.

The limit form of the derivative by definition *implies continuity* (using the product rule):
$$
\begin{aligned}
\lim_{x\rightarrow a}\left(\phi(x)-\phi(a)\right) 
&= \lim_{x\rightarrow a}\left(x-a\right) \frac{\phi(x)-\phi(x)}{x-a}\\
&= \lim_{x\rightarrow a}\left(x-a\right)\cdot\lim_{x\rightarrow a}\frac{\phi(x)-\phi(x)}{x-a}\\
&= 0\cdot\lim_{x\rightarrow a}\frac{\phi(x)-\phi(x)}{x-a}\\
&= 0\;\qed
\end{aligned}
$$

Multivariable
-------------
Let $A\subset \mathbb{R}^m$, and $f\colon A\rightarrow\mathbb{R}^n$. Suppose that $A$ contains a neighbourhood of $a$, then for some $\vb{u} \in \mathbb{R}^m$ we define the directional derivative of $f$ at $\vb{a}$ wih respect to $\vb{u}$ as
$$
    \tag{2}
    \Delta_\vb{u} f = \lim_{t\rightarrow 0}\frac{f(\vb{a}+t\vb{u})-f(\vb{a})}{t}\,,
$$
provided that the limit exists.

We can equally recast the definition of differentiability for a single variable function, and instead state that $\phi$ is differentiable at $a$ if there exists $\lambda \in \mathbb{R}$ such that 
$$
    \frac{\phi(a+t)-\phi(a)-\lambda t}{t} \rightarrow 0 \quad\text{as}\quad t\rightarrow 0\,.
$$
$\lambda$, which is unique, is called the derivative of $\phi$ at $a$ denoted $\phi'(a)$. This definition may then be generalised to higher dimenion. 

We state that $f$ is differentiable at $\vb{a}$ if there exists an $n\times m$ matrix $B$ such that 
$$
    \tag{3}
    \frac{f(\vb{a}+\vb{h})-f(\vb{a})-B\cdot\vb{h}}{\abs{\vb{h}}}\rightarrow 0\quad\text{as}\quad \vb{h}\rightarrow \vb{0}\,.
$$
As before, **$B$ is called the derivative of $f$ at $\vb{a}$ denoted $Df(\vb{a})$**. $B$ is observably unique: consider another matrix $C$ satisfying this condition, and let  $\vb{h}=\vu{u}t$. We then have (for **arbitrary** $\vu{u}$)
$$
(C-B)\cdot \vu{u} = \vb{0}\,,
$$
which implies $C=B$. From with $\vb{h}=t\vu{u}$, **(3)** becomes
$$
    \frac{f(\vb{a}+\vb{h})-f(\vb{a})-B\cdot\vu{u}t}{\abs{t}}\rightarrow 0\quad\text{as}\quad t\rightarrow \vb{0}\,.    
%     \Delta_\vb{u}f(\vb{a}) = Df(\vb{a})\cdot\vb{u}
$$
For $t > 0$ and $t < 0$ we have
$$
    \frac{f(\vb{a}+\vb{h})-f(\vb{a})}{t}-B\cdot\vu{u}\rightarrow 0\quad\text{as}\quad t\rightarrow \vb{0}\,.    
%     \Delta_\vb{u}f(\vb{a}) = Df(\vb{a})\cdot\vb{u}
$$
which gives
$$
\tag{4}
\begin{aligned}
     \Delta_\vb{u}f(\vb{a}) 
     &= B\cdot\vu{u}\\
     &= Df(\vb{a})\cdot\vb{u}\,.
\end{aligned}
$$

