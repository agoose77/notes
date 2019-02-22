# Second Order Differential Equations
Consider an equation of the form
$$
    p(t)y^{\prime\prime}+q(t)y^\prime+r(t)y=g(t)\,.
$$

This is a non-homogeneous differential equation of second order. The associated _homogeneous_ equation is 
$$
    p(t)y^{\prime\prime}+q(t)y^\prime+r(t)y = 0 \,.
$$

We can show that a homogeneous linear differential equation of the form 
$$
    y^{(n)}+f_{n-1}(x)y^{(n-1)}+\dots + f_1(x)y^\prime + f_0(x)y = 0
$$

has $n$ linearly independent solutions $y_1,\,y_2,\,\dots,\,y_n$.


<div style="padding:15px;margin-bottom:20px;border:1px solid transparent;border-radius:4px;color:#31708f;background-color:#d9edf7;border-color:#bce8f1;">

#### Dimensionality of Linear ODE Solution Space
Consider a _special [set](set.md) of solutions_ $g_1(x),\,g_2(x),\,\dots,\,g_n(x)$, each satisfying the following conditions
$$
\begin{aligned}
    g_i^{(j)}(x_0) = \begin{cases}
                        1, & \text{if } j = i-1 \\
                        0,               & \text{otherwise}
                    \end{cases}\,.
\end{aligned}
$$
By TODO, each function $g_1,\,g_2,\,\dots,\,g_n$ exists. We can form a linear combination of this special set of solutions, set it to zero, and take its successive derivatives
    
<!-- todo move from g_1 -> g_n to g_0 -> g_{n-1} -->
    
$$
\begin{aligned}
c_1g_1(x)+c_2g_2(x)+\dots+c_ng_n(x) &= 0 \\
c_1g_1^\prime(x)+c_2g_2^\prime(x)+\dots+c_ng_n^\prime(x) &= 0 \\
&\;\;\vdots\\
c_1g_1^{(n-1)}(x)+c_2g_2^{(n-1)}+\dots+c_ng_n^{(n-1)}(x) &= 0 
\end{aligned}
$$

If we let $x=x_0$, then by the initial conditions, the first linear combination in $\{\,g_i^{(0)}\,\}$ reduces to $c_1=0$, the combination in $\{\,g_i^{(1)}\,\}$ reduces to $c_2=0$, $\dots$, and the final combination in $\{\,g_i^{(n-1)}\,\}$ reduces to $c_n=0$. Hence, for $x=x_0\in I$, $g_1,\,g_2,\,\dots,\,g_n$ is a _linearly independent_ set. Since each function is a solution to the linear ODE, we have $n$ linearly independent solutions.
    
    <!-- p 787 -->
</div>