# Abel's Theorem

## Theorem

Consider a homogeneous linear second order ODE

$$
\tag{a}
y^{\prime\prime} + p(x)y^\prime + q(x)y = 0\,,
$$

on the interval $I\subseteq\mathbb{R}$, where $p(x),\,q(x)$ are real or complex valued continuous functions.

Let $y_1,\,y_2$ be two solutions of **(a)**.
The [Wronskian](wronskian.md) of $y_1,\,y_2$ satisfies the relation

$$
\operatorname W[y_1,y_2](x)=C(x_0)\exp\mathopen{}\left(-\int_{x_0}^xp(t)\,\mathrm{d}t\right)\mathclose{}\,\forall\,x,x_0\in I\,,
$$

where

$$
\operatorname{W}[y_1,y_2] = \begin{vmatrix}y_1(x) & y_2(x)\\y_1^\prime(x) & y_2^\prime(x)\end{vmatrix}\,.
$$

## Proof

Differentiating the Wronskian using the product rule gives

$$
\tag{b}
\begin{aligned}
\operatorname{W}^\prime &= y_1^\prime y_2^\prime+y_1y_2^{\prime\prime}-y_2^\prime y_1^\prime-y_2y_1^{\prime\prime}\\
&= y_1y_2^{\prime\prime} - y_2y_1^{\prime\prime}\,.
\end{aligned}
$$

Solving **(a)** for $y^{\prime\prime}$, we find $y^{\prime\prime}=-(py^\prime+qy)$. Substituting this result into **(b)**, it follows that

$$
\begin{aligned}
\operatorname{W}^\prime &= -y_1(py_2^\prime+qy_2) + y_2(py_1^\prime+qy_1)\\
&= -p(y_1 y_2^\prime - y_1^\prime y_2)\\
&= -p\operatorname{W}\,.
\end{aligned}
$$

This is first order linear ODE, which can be solved. Since $p(x)$ is continuous on $I$, it is _integrable_, and hence

$$
\operatorname{W}(x) = \operatorname{W}(x_0)\exp\mathopen{}\left(-\int_{x_0}^xp(x)\,\mathrm{d}x\right)\mathclose{}\,.
$$

For $\operatorname{W}(x)$ to vanish _anywhere_ then $\operatorname{W}(x_0)=0$, as there is no $u$ such that $\exp(u)=0$. If $\operatorname{W}(x_0)=0$ then $\operatorname{W}(x)=0\,\forall\,x\in I$.
