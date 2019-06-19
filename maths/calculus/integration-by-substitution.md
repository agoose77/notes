# Integration By Substitution

## Single Variable

### Theorem

- Let $\phi$ be a real function with a derivative, on the closed interval $[a, b]$.
- Let $I$ be an _open interval_ which contains the image of $[a, b]$ under $\phi$.
- Let $f$ be a real function which is continuous on $I$.

Then

$$
\int_{\phi(a)}^{\phi(b)}f(t)\,\mathrm{d}t = \int_a^b f\big(\phi(u)\big)\phi^\prime(u)\,\mathrm{d}u\,,
$$

and

$$
\int f(x)\,\mathrm{d}x = \int f\big(\phi(u)\big)\phi^\prime(u) \,\mathrm{d}u\,,
$$

where $x = \phi(u)$.

### Proof

#### Indefinite Integrals

Let $F(u) = \int f(u)\,\mathrm{d}u$. By definition, $F(u)$ is an [antiderivative](fundamental-theorem-of-calculus.md#The-Antiderivative) of $f(u)$.

Hence, by the chain rule,

$$
\tag{a}
\begin{aligned}
    \frac{\mathrm{d}}{\mathrm{d}u}F\big(\phi(u)\big) &= F^\prime\big(\phi(u)\big)\phi^\prime(u)\\
                                             &= f\big(\phi(u)\big)\phi^\prime(u)\,.
\end{aligned}
$$

Evidently, $F(u)$ is an antiderivative of $f\big(\phi(u)\big)\phi^\prime(u)$, therefore

$$
    \int f\big(\phi(u)\big)\phi^\prime(u) \,\mathrm{d}u = F\big(\phi(u)\big) = \int f(x)\,\mathrm{d}x\,,
$$

where $x = \phi(u)$.

#### Definite Integrals

As before, $F(u)$ is an antiderivative of $f$. From the chain rule, we obtain **(a)**. Hence, from [the fundamental theorem of calculus](fundamental-theorem-of-calculus.md#Second-Fundamental-Theorem-of-Calculus):

$$
    \int_a^b f\big(\phi(u)\big)\phi^\prime(u)\,\mathrm{d}u = \left[F\big(\phi(u)\big)\right]_a^b\,.
$$

However, by the same rule,

$$
\begin{aligned}
    \int_{\phi(a)}^{\phi(b)}f(t)\,\mathrm{d}t &= \left[F(t)\right]_{\phi(a)}^{\phi(b)}\\
                                              &= \int_a^b f\big(\phi(u)\big)\phi^\prime(u)\,\mathrm{d}u\,.
\end{aligned}
$$

## Multiple Variables

Consider a transformation $T:\mathbb{R}^2\rightarrow\mathbb{R}$ which maps from $(u,v)$ to $(x,y)$, where $x=g(u,v),y=h(u,v)$.

If $S\subseteq \mathbb{R}^2$ is a region in the $uv$ plane, on which $T$ is a one-to-one function, and $R=T(S)$, we might look to find an expression which relates an integral using $xy$ coordinates on $R$ to one using $uv$ coordinates on $S$.

Let us define a small rectangle $L$ in a region of $S$, with vertices $\vb{o},\vb{p},\vb{q}$. Under $T$, the image of $L$ may be approximated (by Taylor expansion to first order) as:

|  Vertex   |    Coordinate    |                  Transformation                  |
| :-------: | :--------------: | :----------------------------------------------: |
| $\vb{o}$ |     $(u,v)$      |            $\big(g(u,v),h(u,v)\big)$             |
| $\vb{p}$ |  $(u+\Delta u)$  | $\left(g(u,v)+\frac{\partial g}{\partial u}\Big | _{u,v}\Delta u,h(u,v)+\frac{\partial h}{\partial u}\Big | _{u,v}\Delta u\right)$ |
| $\vb{q}$ | $(u,v+\Delta v)$ | $\left(g(u,v)+\frac{\partial g}{\partial v}\Big | _{u,v}\Delta v,h(u,v)+\frac{\partial h}{\partial v}\Big | _{u,v}\Delta v\right)$ |

If we assume that $T$ is linear, then the image of $L$ under $T$ is a parallelogram with sides $\vb{p}-\vb{o}$, and $\vb{q}-\vb{o}$. We can find its area by calculating the cross product:

$$
\begin{vmatrix}
\vu{i} & \vu{j} & \vu{k}\\
\frac{\partial g}{\partial u}(u,v)\Delta u & \frac{\partial h}{\partial u}(u,v)\Delta u & 0\\
\frac{\partial g}{\partial v}(u,v)\Delta v & \frac{\partial h}{\partial v}(u,v)\Delta v & 0\\
\end{vmatrix} =
\left(\frac{\partial g}{\partial u}(u,v)\frac{\partial h}{\partial v}(u,v)- \frac{\partial h}{\partial u}(u,v)\frac{\partial g}{\partial v}(u,v)\right)\Delta u \Delta v \vu{k}\,,
$$

whose $\vb{k}$ component is the determinant of the _Jacobian matrix_ $J_T(u,v)$ of $T$, which is defined as

$$
J_T(u_1, \dots, u_n)=
\begin{bmatrix}
    \frac{\partial x_1}{\partial u_1} & \frac{\partial x_2}{\partial u_1} & \dots & \frac{\partial x_n}{\partial u_1}\\
    \frac{\partial x_1}{\partial u_2} & \frac{\partial x_2}{\partial u_2} & \dots & \frac{\partial x_n}{\partial u_2}\\
    \vdots & \vdots & \ddots & \vdots\\
\frac{\partial x_1}{\partial u_n} & \frac{\partial x_2}{\partial u_n} & \dots & \frac{\partial x_n}{\partial u_n}
\end{bmatrix}\,.
$$

Evidently, the region $L$ has area $\Delta u \Delta v$ in $S$, and an area $\lvert \operatorname{det}J_T(u,v)\rvert \Delta u\Delta v$ in $T(S)$.
Hence, a double integral over $R$

$$
\iint\limits_Rf(x,y)\,\mathrm{d}A=\iint\limits_Rf(x,y)\,\mathrm{d}x\,\mathrm{d}y\,,
$$

can be transformed to an integral over $S$

$$
\iint\limits_Sf(g(u,v),h(u,v))\,\mathrm{d}A=\iint\limits_Sf(g(u,v),h(u,v))\lvert \operatorname{det}J_T(u,v)\rvert\,\mathrm{d}u\,\mathrm{d}v\,.
$$
