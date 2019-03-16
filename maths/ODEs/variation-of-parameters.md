Variation of Parameters
=======================
Recall that the complementary function for some _non homogeneous_ linear ODE of second order is  $y_c = c_1y_1 + c_2y_2$ , where $y_1,\,y_2$ are linearly independent solutions of the associated _homogeneous_ equation. For a linear ODE, the [general solution](n-order-general-solution.md) is given by $y=y_c+y_p$, which reduces to $y_c$ for the homogeneous linear ODE where $y_p=0$.

For the nonhomogeneous linear ODE 
$$
    \tag{a}
    s(t)y^{\prime\prime}(t) + y^\prime p(t) + q(t)y(t) = g(t)\,,
$$
let us define 
$$
    \tag{b}
    y_p(t) = u_1(t)y_1(t) + u_2(t)y_2(t)\,.
$$
Taking the derivative of **(b)**, 
$$
    {y_p}^\prime(t) = u_1(t){y_1}^\prime(t) + {u_1}^\prime(t)y_1(t) + u_2(t){y_2}^\prime(t) + {u_2}^\prime(t)y_2(t)\,,
$$
we assume that ${u_1}^\prime(t)y_1(t) + {u_2}^\prime(t)y_2(t) = 0$, such that
$$
\begin{aligned}
    {y_p}^\prime(t) &= u_1(t){y_1}^\prime(t) + u_2(t){y_2}^\prime(t)\\
    y_p^{\prime\prime}(t) &= u_1(t)y^{\prime\prime}(t) + {u_1}^\prime(t){y_1}^\prime(t) + u_2(t)y_2^{\prime\prime}(t) + {u_2}^\prime(t){y_2}^\prime(t)\,.
\end{aligned}
$$
**(a)** may then be rewritten as 
$$
    s(t)\left(u_1(t)y^{\prime\prime}(t) + {u_1}^\prime(t){y_1}^\prime(t) + u_2(t)y_2^{\prime\prime}(t) + {u_2}^\prime(t){y_2}^\prime(t)\right) + p(t)\left(u_1(t){y_1}^\prime(t) + u_2(t){y_2}^\prime(t)\right) + q(t)\left(u_1(t)y_1(t) + u_2(t)y_2(t)\right)
$$