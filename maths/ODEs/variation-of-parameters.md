'xrandr --output DP-1-2-1 --rotate left --pos 1920x0 --output DP-1-2-3 --pos 0x427'Variation of Parameters
=======================
Recall that the complementary function for some _non homogeneous_ linear ODE of second order is  $y_c = c_1y_1 + c_2y_2$ , where $y_1,\,y_2$ are linearly independent solutions of the associated _homogeneous_ equation. For a linear ODE, the [general solution](n-order-inhomogeneous-general-solution.md) is given by $y=y_c+y_p$, which reduces to $y_c$ for the homogeneous linear ODE where $y_p=0$.

For the nonhomogeneous linear ODE 
$$
    \tag{a}
    s(t)y^{\prime\prime}(t) + y^\prime(t) p(t) + q(t)y(t) = g(t)\,,
$$
let us define 
$$
    \tag{b}
    y_p = u_1y_1 + u_2y_2\,.
$$
Taking the derivative of **(b)**, 
$$
    {y_p}^\prime = u_1{y_1}^\prime + {u_1}^\prime y_1 + u_2{y_2}^\prime + {u_2}^\prime y_2\,,
$$
we assume that 
$$
    \tag{c}
    {u_1}^\prime y_1 + {u_2}^\prime y_2 = 0\,,
$$ such that
$$
\begin{aligned}
    {y_p}^\prime &= u_1{y_1}^\prime + u_2{y_2}^\prime\\
    y_p^{\prime\prime} &= u_1y^{\prime\prime} + {u_1}^\prime{y_1}^\prime + u_2y_2^{\prime\prime} + {u_2}^\prime{y_2}^\prime\,.
\end{aligned}
$$
**(a)** may then be rewritten as 
$$
    s\Big(u_1y^{\prime\prime} + {u_1}^\prime{y_1}^\prime + u_2y_2^{\prime\prime} + {u_2}^\prime{y_2}^\prime\Big) + 
    p\Big(u_1{y_1}^\prime + u_2{y_2}^\prime\Big) + 
    q\Big(u_1y_1 + u_2y_2\Big) = g\,.
$$

Grouping terms in $u_1$, $u_2$,
$$
    \tag{d}
    s\Big({u_1}^\prime{y_1}^\prime + {u_2}^\prime{y_2}^\prime\Big) + 
    u_1\Big(s{y_1}^{\prime\prime} + p{y_1}^\prime + qy_1\Big) + 
    u_1\Big(s{y_1}^{\prime\prime} + p{y_1}^\prime + qy_1\Big) = g\,.
$$

As $y_1,\,y_2$ are solutions to the _homogeneous_ equation, it follows that **(d)** reduces to
$$
    {u_1}^\prime{y_1}^\prime + {u_2}^\prime{y_2}^\prime  = \frac{g}{s}\,.
$$

Let us now _redefine_ $p, q, g$ such that $s$ is divided out,
$$
    \tag{d}
    {u_1}^\prime{y_1}^\prime + {u_2}^\prime{y_2}^\prime  = g\,.
$$

From **(c\)**, ${u_1}^\prime=\frac{-{u_2}^\prime}{y_1}y_2$, hence **(d)** becomes
$$
\begin{aligned}
    -\frac{{u_2}^\prime}{y_1}y_2{y_1}^\prime + {u_2}^\prime{y_2}^\prime &= g(t)\\
    {u_2}^\prime \left({y_2}^\prime-\frac{y_2}{y_1}{y_1}^\prime\right) &= g(t)\\
    {u_2}^\prime \left(\frac{{y_2}^\prime y_1-y_2{y_1}^\prime}{y_1}\right) &= g(t)\,,
\end{aligned}
$$
hence
$$
    {u_2}^\prime = \frac{g(t)y_1}{\operatorname{W}\mathopen{}\big[y_1,y_2\big]\mathclose{}}\,.
$$

Given that $y_1,\,y_2$ form a _fundamental set of solutions_, it follows from [Abel's theorem](abels-theorem.md) that $\operatorname{W}\mathopen{}\big[y_1,y_2\big]\mathclose{}$ is exclusively either zero or non-zero for _all_ $t \in I$.
un
<div style="padding:15px;margin-bottom:20px;border:1px solid transparent;border-radius:4px;color:#31708f;background-color:#d9edf7
;border-color:#bce8f1;">

#### Non Vanishing Wronskian for solutions to Non-Singular Second Order ODEs
Suppose that the Wronskian $\operatorname W[f,g](x)$ vanished at some point $x_1$. Then the vectors $\begin{bmatrix}f(x_1)\\f^\prime(x_1)\\\end{bmatrix}$ and $\begin{bmatrix}g(x_1)\\g^\prime(x_1)\\\end{bmatrix}$ would be linearly dependent, and therefore proportional: $g(x_1)=kf(x_1)$ and $g^\prime(x_1)=kf^\prime(x_1)$ for some constant $k$. Now consider the function $h(x)=g(x)-kf(x)$. This function is a solution to the DE 
$$
    \tag{e}
    u^{\prime\prime} + p(x)u^\prime + q(x)u = 0\,,
$$
since it is a linear combination of solutions $f,\,g$. It also satisfies the initial conditions $h(x_1)=h^\prime(x_1)=0$. From [the uniqueness theorem](n-order-existence-theorem.md), there can only be _one_ solution to **(e)** with initial conditions $u(x_1)=u_1$,$u^\prime(x_1)=u^\prime_1$. It follows that $f(x)=kg(x)\,\forall\,x\in I$
    TODO
</div>

<!-- Can the Wronskian be nonzero for linearly _depedendent_ fns? -->