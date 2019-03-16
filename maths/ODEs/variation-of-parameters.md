Variation of Parameters
=======================
Recall that the complementary function for some _non homogeneous_ linear ODE of second order is  $y_c = c_1y_1 + c_2y_2$ , where $y_1,\,y_2$ are linearly independent solutions of the associated _homogeneous_ equation. For a linear ODE, the [general solution](n-order-general-solution.md) is given by $y=y_c+y_p$, which reduces to $y_c$ for the homogeneous linear ODE where $y_p=0$.

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
    \frac{{u_2}^\prime}{y_1}
$$