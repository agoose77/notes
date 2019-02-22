# Curvilinear Coordinates
Curvilinear coordinates are a coordinate system for Euclidean space in which the coordinate lines may be curved. We can define a coordinate in Cartesian space a series of functions of its curvilinear coordinates $(u,v,w)$,
$$
\begin{aligned}
    x &= x(u,v,w)\\
    y &= y(u,v,w)\\
    z &= z(u,v,w)\,.
\end{aligned}
$$
The transformation which maps between the two coordinate systems is locally invertible (a one-to-one map).

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/57/General_curvilinear_coordinates_1.svg/1280px-General_curvilinear_coordinates_1.svg.png" alt="Curvilinear and Cartesian axes superimposed" style="width:400px;margin-bottom:-50px;"/>

The total derivative of a position vector in a curvilinear space is given by
$$
\mathrm{d}\vec{r} = \frac{\partial \vec{r}}{\partial u}\,\mathrm{d}u + 
                    \frac{\partial \vec{r}}{\partial v}\,\mathrm{d}v +
                    \frac{\partial \vec{r}}{\partial w}\,\mathrm{d}w
$$
which represents an infinitesimal displacement in the metric space.


## Basis Vectors
Consider the curve $\Gamma(u)=\vec{r}(u, v_0, w_0)$, where $\vec{r}(u,v,w)$ is the position vector of $(u,v,w)$. Evidently, $\frac{\mathrm{d}\Gamma}{\mathrm{d}u}=\frac{\partial \vec{r}}{\partial u}$ represents a _tangent vector_ $\vec{b}_u$ to $\Gamma(u)$. This can be repeated for $v,w$ to find the tangent vectors $\vec{b_\Omega}$ ($\forall \Omega\in\{\, u,v,w\,\}$) to the $u,v,w$ curves: 
$$
\vec{b_\Omega}=\frac{\partial \vec{r}}{\partial \Omega}\,.
$$

We can determine the basis vectors $\vec{\hat{e}_\Omega}$ by normalising $\vec{b_\Omega}$. If we the _metrical coefficients_ as $h_\Omega=\lvert \frac{\partial \vec{r}}{\partial \Omega} \rvert$, then $\vec{\hat{e}_\Omega} = \frac{1}{h_\Omega}\frac{\partial \vec{r}}{\partial \Omega}$. This gives
$$
\mathrm{d}\vec{r} = h_u\mathrm{d}u\,\vec{\hat{e}_u} + 
                    h_v\mathrm{d}v\,\vec{\hat{e}_v} + 
                    h_w\mathrm{d}w\,\vec{\hat{e}_w}\,.
$$

## Line and Volume Elements
From this it follows that the line element is given by
$$
\mathrm{d}l = \sqrt{\mathrm{d}\vec{r}\cdot\mathrm{d}\vec{r}}=\sqrt{\sum_i\left(h_i\mathrm{d}\Omega_i\right)^2}
$$

Similarly, the surface element is given by the magnitude of the cross product
$$
\mathrm{d}S=\lvert\mathrm{d}\vec{r}_u\,\vec{\hat{e}_u}\times\mathrm{d}\vec{r}_v\,\vec{\hat{e}_v}\rvert\,.
$$

The volume element can be found from the absolute value of the triple product
$$
\mathrm{d}V=\left\lvert\mathrm{d}\vec{r}_u\,\vec{\hat{e}_u}\cdot\left(\mathrm{d}\vec{r}_v\,\vec{\hat{e}_v}\times\mathrm{d}\vec{r}_w\,\vec{\hat{e}_w}\right)\right\rvert=h_uh_vh_w\,\mathrm{d}u\,\mathrm{d}v\,\mathrm{d}w\,.
$$
Given that $\mathrm{d}\vec{r}_\Omega\vec{\hat{e}_\Omega}=\frac{\partial \vec{r}}{\partial \Omega}\,\mathrm{d}\Omega$, the volume element may also be written as 
$$
\begin{aligned}
\mathrm{d}V&=\left\lvert
\frac{\partial \vec{r}}{\partial u}
\cdot
\left(
    \frac{\partial \vec{r}}{\partial v}
    \times
    \frac{\partial \vec{r}}{\partial w}
\right)
\right\rvert\mathrm{d}u\,\mathrm{d}v\,\mathrm{d}w\\
&=
\begin{vmatrix}
\frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} & \frac{\partial x}{\partial v} \\
\frac{\partial y}{\partial u} & \frac{\partial y}{\partial v} & \frac{\partial y}{\partial v} \\
\frac{\partial z}{\partial u} & \frac{\partial z}{\partial v} & \frac{\partial z}{\partial v} \\
\end{vmatrix}\mathrm{d}u\,\mathrm{d}v\,\mathrm{d}w\\
&= \lvert J\rvert\,\mathrm{d}u\,\mathrm{d}v\,\mathrm{d}w\,,
\end{aligned}
$$
where $J$ is the [Jacobian matrix](integration-by-substitution.md) of the transformation.