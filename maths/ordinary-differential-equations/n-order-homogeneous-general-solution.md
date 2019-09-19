# The General Solution to an Homogeneous Linear ODE of Order $n$

## Theorem

If $y_1,\,y_2,\,\dots,\,y_n$ are linearly independent solutions of the homogeneous linear ODE

$$
\tag{a}
     y^{(n)} + f_{n-1}(x)y^{(n-1)} + \dots + f_0(x)y=0\,,
$$

then the _complementary function_

$$
\tag{b}
y_c = c_1 y_1 + c_2 y_2 + \dots + c_n y_n\,,
$$

is a _general solution_ of **(a)** and $\{\,y_1,\,y_2,\,\dots,\,y_n\,\}$ form a _fundamental set_ of solutions, i.e. every solution of **(a)** can be obtained from **(b)** by proper choice of the constants $c_1,\,c_2,\,\dots,\,c_n$.

## Proof

Given that $y_1,\,y_2,\,\dots,\,y_n$ are solutions to **(a)**, there are $n$ differential equations

$$
\begin{aligned}
     y_1^{(n)} + f_{n-1}(x)y_1^{(n-1)} + \dots + f_0(x)y_1 &= 0\\
     y_2^{(n)} + f_{n-1}(x)y_2^{(n-1)} + \dots + f_0(x)y_2 &= 0\\
     &\;\;\vdots\\
     y_n^{(n)} + f_{n-1}(x)y_n^{(n-1)} + \dots + f_0(x)y_n &= 0\,.
\end{aligned}
$$

Taking a linear combination of these equations, it follows that

$$
\begin{aligned}
     c_1y_1^{(n)} + c_1f_{n-1}(x)y_1^{(n-1)} + \dots + c_1f_0(x)y_1 &+{}\\
     c_2y_2^{(n)} + c_2f_{n-1}(x)y_2^{(n-1)} + \dots + c_2f_0(x)y_2 &+{}\\
     &\;\;\vdots\\
     c_ny_n^{(n)} + c_nf_{n-1}(x)y_n^{(n-1)} + \dots + c_nf_0(x)y_n &= 0\,.
\end{aligned}
$$

Let us group the terms in $f_i(x)$

$$
\begin{aligned}
     c_1y_1^{(n)} + c_2y_2^{(n)} + \dots + c_ny_n^{(n)} &+ {} \\
     f_{n-1}(x)\left(c_1y_1^{(n-1)} + c_2y_2^{(n-1)} + \dots + c_ny_n^{(n-1)}\right) &+ {} \\
     &\;\;\vdots\\
     f_{0}(x)\left(c_1y_1 + c_2y_2 + \dots + c_ny_n\right) &= 0\,.
\end{aligned}
$$

Evidently this is just **(a)** with $y=y_c$, hence $y_c$ is also a solution to **(a)**.

<!-- TODO: Abel's theorem required

---
First we shall prove the theorem for $n = 2$. Let $y_1,\,y_2$ be two linearly independent solutions of
$$
    \tag{c}
    y^{\prime\prime} + f_1(x) y^\prime + f_0(x) y = 0\,.
$$
-->
