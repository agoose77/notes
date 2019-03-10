Constrained Optimisation
========================

## Lagrange multipliers
In general, the method of Lagrange multipliers is convert a constrained optimisation problem into an unconstrained one. Consider the case where one wishes to find the stationary points of some function $f(\vec{x})$ where $\vec{x}=(x_1,x_2,\dots,x_N)^\mathsf{T}$, subject to the constraints $g_k(\vec{x})=0$ for $k=1,\dots,m<N$.
First, one must form the Lagrangian
$$
    \mathcal{L}(\vec{x}, \vec{\lambda}) = f(\vec{x}) + \sum^m_{k=1}\lambda_k g_k(\vec{x})\,,
$$
  where $\vec{\lambda}=(\lambda_1, \lambda_2, \dots, \lambda_m)^\mathsf{T}$ are the \textit{Lagrange multipliers}. The partial derivatives of $\mathcal{L}$ with respect to its dependent variables are then
$$
    \begin{aligned}
    \frac{\partial \mathcal{L}}{\partial x_j}&=\frac{\partial f}{\partial x_j}+\sum_{k=1}^m\lambda_k\frac{\partial g_k}{\partial x_j}\\
    \frac{\partial \mathcal{L}}{\partial \lambda_k} &= g_k\,.
  \end{aligned}
$$
  At the stationary points of $\mathcal{L}(\vec{x},\vec{\lambda})$, all of these partial derivatives must be zero, which establishes a set of unconstrained problems to solve. Given that the stationary points $\vec{x}^\prime$ must satisfy the constraint function(s) $g_k(\vec{x})=0$, and hence $\mathcal{L}(\vec{x}^\prime, \vec{\lambda})=f(\vec{x})$, they coincide with the stationary points of $f$.

## Optimising a functional
The method of Lagrange multipliers can be generalised to functionals of the form
$$
J[\vec{y}] = \int_a^bF(x,\vec{y},\vec{y}_x)\,\mathrm{d}x\,,
$$
where $\vec{y}$ is the vector of $N$ functions of the form $y=y(x)$ which extremise $J$,
subject to the set of $m$ constraints, for $k=1,\dots,m<N$:
$$
G_k(x,\vec{y})=0\,.
$$
Given that $G(x, \vec{y})$ must hold for all $x$, it follows that
$$
\int_a^b\lambda_k(x)G_k(x, \vec{y})\,\mathrm{d}x=0\,.
$$
One can define a new functional
$$
\begin{aligned}
\tilde{J}[\vec{y},\vec{\lambda}] &= \int_a^bF(x,\vec{y},\vec{y}_x)\,\mathrm{d}x+
\sum_{k=1}^m\int_a^b\lambda_k(x)G_k(x,\vec{y})\,\mathrm{d}x\\
&= \int_a^b\left(F(x,\vec{y},\vec{y}_x)+
\sum_{k=1}^m\lambda_k(x)G_k(x,\vec{y})\right)\,\mathrm{d}x\\
  &= \int_a^b\tilde{F}(x,\vec{y},\vec{y}_x,\vec{\lambda})\,\mathrm{d}x\\
\end{aligned}
$$
where $\vec{\lambda}=(\lambda_1(x),\lambda_2(x),\dots,\lambda_m(x))^\mathsf{T}$ is a vector of $m$ Lagrange multiplier \textit{functions}. As for the classical variational problem, if $(\vec{y},\vec{\lambda})$ extremise $\tilde{F}$, then $\tilde{F}$ must satisfy the Euler\textendash Lagrange equations for all independent variables,
$$
\begin{aligned}
\frac{\partial\tilde{F}}{\partial y_i}-\frac{\mathrm{d}}{\mathrm{d}x}\left(\frac{\partial \tilde{F}}{\partial y_i^\prime}\right)&=0\\
\frac{\partial \tilde{F}}{\partial \lambda_k}-\frac{\mathrm{d}}{\mathrm{d}x}\left(\frac{\partial \tilde{F}}{\partial \lambda_k^\prime}\right)&=0\,.
\end{aligned}
$$
Given that $\tilde{F}$ is independent of $\vec*{\lambda}^\prime$, and $\frac{\partial \tilde{F}}{\partial \lambda_k}=G_k(x, \vec{y})$, one has to solve the following relations
$$
\begin{aligned}
\frac{\partial \tilde{F}}{\partial y_i}-\frac{\mathrm{d}}{\mathrm{d}x}\left(\frac{\partial \tilde{F}}{\partial y_i^\prime}\right)&=0\\
G_k(x,\vec{y})&=0\,.
\end{aligned}
$$

### Integral Constraints
Where the constraints are already in integral form such that
$$
\int_a^bG(x,\vec{y})\,\mathrm{d}x=0\,,
$$
for $k=1,\dots,m$ as before, the modified functional is
$$
\begin{aligned}
\tilde{J}[\vec{y},\vec*{\lambda}]&=J[\vec{y}]+\sum_{k=1}^m\lambda_k\int_a^bG_k(x,\vec{y})\,\mathrm{d}x\\
                             &=\int_a^b\left(F(x,\vec{y},\vec{y}_x)+\sum_{k=1}^m\lambda_kG_k(x,\vec{y})\right)\,\mathrm{d}x\,.
\end{aligned}
$$
Given that the Euler\textendash Lagrange equations only hold for functions which extremise the functional ($\mathcal{S}, J, \dots$), there is only one set of solutions
$$
\begin{aligned}
\frac{\partial \tilde{F}}{\partial y_i}-\frac{\mathrm{d}}{\mathrm{d}x}\left(\frac{\partial \tilde{F}}{\partial y_i^\prime}\right)&=0\,.\\
\end{aligned}
$$


## Useful Links
* http://www.macs.hw.ac.uk/~simonm/mechanics.pdf