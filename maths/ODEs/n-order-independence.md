<!-- 65.4 p786 -->

# Linear Independence of Solutions to a Linear ODE of Order $n$

## Theorem

If $f_0(x),\,f_1(x),\,\dots,\,f_n(x)$ are each continuous functions of $x$ on a common interval $I$, then the homogeneous linear ODE

$$
\tag{a}
     y^{(n)} + f_{n-1}(x)y^{(n-1)} + \dots + f_0(x)y=0
$$

has $n$ linearly independent solutions $y_1,\,y_2,\,\dots,\,y_n$.

## Proof

Consider a _special [set](../set.md) of solutions_ $g_1(x),\,g_2(x),\,\dots,\,g_n(x)$, each satisfying the following conditions

$$
\begin{aligned}
    g_i^{(j)}(x_0) = \begin{cases}
                        1, & \text{if } j = i-1 \\
                        0,               & \text{otherwise}
                    \end{cases}\,.
\end{aligned}
$$

By [the uniqueness theorem](n-order-existence-theorem.md#Existence-and-Uniqueness-Theorem-for-a-Linear-ODE-of-Order-%24n%24), each function $g_1,\,g_2,\,\dots,\,g_n$ exists for its unique set of initial conditions. We can form a linear combination of this special set of solutions, set it to zero, and take its successive derivatives

<!-- todo move from g_1 -> g_n to g_0 -> g_{n-1} -->

$$
\begin{aligned}
c_1g_1(x)+c_2g_2(x)+\dots+c_ng_n(x) &= 0 \,,\\
c_1g_1^\prime(x)+c_2g_2^\prime(x)+\dots+c_ng_n^\prime(x) &= 0\,, \\
&\;\;\vdots\\
c_1g_1^{(n-1)}(x)+c_2g_2^{(n-1)}+\dots+c_ng_n^{(n-1)}(x) &= 0 \,.
\end{aligned}
$$

If we let $x=x_0$, then by the initial conditions, the first linear combination in $g_i^{(0)}$ reduces to $c_1=0$, the combination in $\,g_i^{(1)}\,$ reduces to $c_2=0$, $\dots$, and the final combination in $g_i^{(n-1)}$ reduces to $c_n=0$. Hence, for $x=x_0\in I$, $g_1,\,g_2,\,\dots,\,g_n$ is a _linearly independent_ set. Since each function is a solution to the linear ODE, we have $n$ linearly independent solutions.

Let

$$
    h(x) = y(x_0)g_1(x) + y^\prime(x_0)g_2(x) + \dots + y^{(n-1)}(x_0)g_n(x)
$$

be another general solution to our ODE, given that $g_1,\,g_2,\,\dots,\,g_n$ is a linearly independent set and that the ODE is linear. Taking successive derivatives of $h(x)$, we obtain

$$
\begin{aligned}
h^\prime(x) &= y(x_0)g_1^\prime(x)+y^\prime(x_0) g_2^\prime(x) + \dots + y^{(n-1)}(x_0)g_n^\prime(x)\,,\\
h^{\prime\prime}(x) &= y(x_0)g_1^{\prime\prime}(x)+y^\prime(x_0) g_2^{\prime\prime}(x) + \dots + y^{(n-1)}(x_0)g_n^{\prime\prime}(x)\,,\\
&\;\;\vdots\\
h^{\prime\prime}(x) &= y(x_0)g_1^{(n-1)}(x)+y^\prime(x_0) g_2^{(n-1)}(x) + \dots + y^{(n-1)}(x_0)g_n^{(n-1)}(x)\,.
\end{aligned}
$$

If we then let $x=x_0$, then once again, the initial conditions simplify the problem, with

$$
\begin{aligned}
    h^\prime(x_0) &= y^\prime(x_0)\,\\
    h^{\prime\prime}(x_0) &= y^{\prime\prime}(x_0)\,\\
    &\;\;\vdots\\
    h^{(n-1)}(x_0) &= y^{(n-1)}(x_0)\,.\\
\end{aligned}
$$

This result shows that $h(x),\;y(x)$ (and their $n-1$ derivatives) are equal when $x=x_0$. By the [uniqueness theorem](n-order-existence-theorem.md#Existence-and-Uniqueness-Theorem-for-a-Linear-ODE-of-order-%24n%24), $h(x)$ is identical to $y(x)$ for $x=x_0$, and hence we can replace $h(x_0)$ with $y(x_0)$

$$
y(x) = y(x_0)g_1(x) + y^\prime(x_0)g_2(x) + \dots + y^{(n-1)}(x_0)g_n(x)\,,
$$

where $x_0\in I$.
  
As that $y(x)$ is a general solution to **(a)**, it follows that every solution to **(a)** may be expressed in this form

$$
\tag{b}
\begin{aligned}
y_1(x) &= y_1(x_0)g_1(x) + y_1^\prime(x_0)g_2(x) + \dots + y_1^{(n-1)}(x_0)g_n(x)\\
y_2(x) &= y_2(x_0)g_1(x) + y_2^\prime(x_0)g_2(x) + \dots + y_2^{(n-1)}(x_0)g_n(x)\\
&\;\;\vdots\\
y_n(x) &= y_n(x_0)g_1(x) + y_n^\prime(x_0)g_2(x) + \dots + y_n^{(n-1)}(x_0)g_n(x)\,,
\end{aligned}
$$

which in matrix form gives

$$
\begin{bmatrix}y_1(x) & y_2(x) & \dots & y_n(x)\end{bmatrix}=
\begin{bmatrix}
y_1(x_0) & y_1^\prime(x_0) & \dots & y_1^{(n-1)}(x_0) \\
y_2(x_0) & y_2^\prime(x_0) & \dots & y_2^{(n-1)}(x_0) \\
\vdots&\vdots&\ddots&\vdots\\
y_n(x_0) & y_n^\prime(x_0) & \dots & y_n^{(n-1)}(x_0) \\
\end{bmatrix}
\begin{bmatrix}
g_1(x) \\ g_2(x) \\ \vdots \\ g_n(x)
\end{bmatrix}
$$

Given that $g_1,\,g_2,\,\dots,\,g_n$ are linearly independent, **(b)** can be solved in terms of $y_1,\,y_2,\,\dots,\,y_n$. This means that, the matrix of the coefficients is invertible,

$$
\tag{c}
\begin{vmatrix}
y_1(x_0) & y_1^\prime(x_0) & \dots & y_1^{(n-1)}(x_0) \\
y_2(x_0) & y_2^\prime(x_0) & \dots & y_2^{(n-1)}(x_0) \\
\vdots&\vdots&\ddots&\vdots\\
y_n(x_0) & y_n^\prime(x_0) & \dots & y_n^{(n-1)}(x_0) \\
\end{vmatrix}\neq 0\,.
$$

Using the elementary row and column operations, we can rearrange **(c)** to give equivalently

$$
\tag{d}
\begin{vmatrix}
y_1(x_0) & y_2(x_0) & \dots & y_n(x_0) \\
y_1^\prime(x_0) & y_2^\prime(x_0) & \dots & y_n^\prime(x_0) \\
\vdots&\vdots&\ddots&\vdots\\
y_1^{(n-1)}(x_0) & y_2^{(n-1)}(x_0) & \dots &  y_n^{(n-1)}(x_0) \\
\end{vmatrix}\neq 0\,.
$$

If the determinant of the [Wronskian](wronskian.md) **(d)** of solutions $y_1,\,y_2,\,\dots,\,y_n$ for some $x=x_0\in I$ is nonzero, then according to the definition of the Wronskian, $y_1,\,y_2,\,\dots,\,y_n$ are linearly independent on $I$.

<!-- p 787 -->

[1]: http://store.doverpublications.com/0486649407.html
