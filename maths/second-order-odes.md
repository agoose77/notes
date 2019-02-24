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


<!-- 65.4 p786 -->
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
c_1g_1(x)+c_2g_2(x)+\dots+c_ng_n(x) &= 0 \,,\\
c_1g_1^\prime(x)+c_2g_2^\prime(x)+\dots+c_ng_n^\prime(x) &= 0\,, \\
&\;\;\vdots\\
c_1g_1^{(n-1)}(x)+c_2g_2^{(n-1)}+\dots+c_ng_n^{(n-1)}(x) &= 0 \,.
\end{aligned}
$$

If we let $x=x_0$, then by the initial conditions, the first linear combination in $\{\,g_i^{(0)}\,\}$ reduces to $c_1=0$, the combination in $\{\,g_i^{(1)}\,\}$ reduces to $c_2=0$, $\dots$, and the final combination in $\{\,g_i^{(n-1)}\,\}$ reduces to $c_n=0$. Hence, for $x=x_0\in I$, $\{\, g_1,\,g_2,\,\dots,\,g_n \,\}$ is a _linearly independent_ set. Since each function is a solution to the linear ODE, we have $n$ linearly independent solutions.

Let
$$
    h(x) = y(x_0)g_1(x) + y^\prime(x_0)g_2(x) + \dots + y^{(n-1)}(x_0)g_n(x)
$$
be another general solution to our ODE, given that $\{\, g_1,\,g_2,\,\dots,\,g_n \,\}$ is a linearly independent set and that the ODE is linear. Taking successive derivatives of $h(x)$, we obtain

$$
\begin{aligned}
h^\prime(x) &= y(x_0)g_1^\prime(x)+y^\prime(x_0) g_2^\prime(x) + \dots + y^{(n-1)}(x_0)g_n^\prime(x)\,,\\
h^{\prime\prime}(x) &= y(x_0)g_1^{\prime\prime}(x)+y^\prime(x_0) g_2^{\prime\prime}(x) + \dots + y^{(n-1)}(x_0)g_n^{\prime\prime}(x)\,,\\
&\;\;\vdots\\
h^{\prime\prime}(x) &= y(x_0)g_1^{(n-1)}(x)+y^\prime(x_0) g_2^{(n-1)}(x) + \dots + y^{(n-1)}(x_0)g_n^{(n-1)}(x)\,.
\end{aligned}
$$
    
If we then let $x=x_0$, then once again our initial conditions simplify the problem, with 

$$
\begin{aligned}
    h^\prime(x_0) &= y^\prime(x_0)\,\\
    h^{\prime\prime}(x_0) &= y^{\prime\prime}(x_0)\,\\
    &\;\;\vdots\\
    h^{(n-1)}(x_0) &= y^{(n-1)}(x_0)\,.\\
\end{aligned}
$$

This result shows that $h(x)=y(x)$ when $x=x_0$. TODO show uniqueness p787.
<!-- p 787 -->
</div>


<!-- 65.4 p786 -->
<div style="padding:15px;margin-bottom:20px;border:1px solid transparent;border-radius:4px;color:#31708f;background-color:#d9edf7;border-color:#bce8f1;">

#### Uniqueness of Solutions to Linear ODEs
Consider a non-homogeneous linear ODE of the form
$$
   f_n(x)y^{(n)} + f_{n-1}(x)y^{(n-1)} + \dots + f_0(x)y=Q(x)\,.
$$
Dividing through by $f_n(x)$, and redefining the terms, it follows that
$$
 y^{(n)} + f_{n-1}(x)y^{(n-1)} + \dots + f_0(x)y=Q(x)\,.
$$
    
Assume that $y(x)$ is a solution. We may then define some additional functions $y_1(x),\,y_2(x),\,\dots,\,y_n(x)$ as follows
$$
\begin{aligned}
y(x) &= y_1(x)\\
y^\prime(x) &= y_1^\prime(x)=y_2(x)\\
y^{\prime\prime}(x) &= y_1^{\prime\prime}(x)=y_2(x)\\
\vdots \\
y^{(n-1)}(x) &= y_1^{(n-1)}(x)=y_2^{(n-2)}(x)=y_n(x)\,.
\end{aligned}
$$

The above relations may be summarised as $y_n(x) = y_{n-1}^\prime(x)$.
    
Hence, $y^{(n)}(x) = y_n^\prime(x)$. From these relations, the ODE may be rewritten as 
$$
    y_n^\prime(x) + f_{n-1}(x)y_n(x) + \dots + f_1(x)y_2(x) + f_0(x)y_1(x) = Q(x)\,,
$$
and thus
$$
    y_n^\prime(x) = -f_{n-1}y_n - \dots - f_1y_2 - f_0y_1 = Q(x)\,.
$$
</div>