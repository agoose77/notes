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

# Line and Volume Elements
The line element on a curvilinear space is
$$
\mathrm{d}\vec{r} = \frac{\partial \vec{r}}{\partial u}\,\mathrm{d}u + 
                    \frac{\partial \vec{r}}{\partial v}\,\mathrm{d}v +
                    \frac{\partial \vec{r}}{\partial w}\,\mathrm{d}w
$$

We can let $\frac{\partial \vec{r}}{\partial \Omega} = \lvert \frac{\partial \vec{r}}{\partial \Omega} \rvert\vec{\hat{e}_\Omega}=h_\Omega\vec{\hat{e}_\Omega}$,
$$
\mathrm{d}\vec{r} = h_u\mathrm{d}u\,\vec{\hat{e}_u} + 
                    h_v\mathrm{d}v\,\vec{\hat{e}_v} + 
                    h_w\mathrm{d}w\,\vec{\hat{e}_w}\,,
$$

which then gives the line element as
$$
\mathrm{d}l = \sqrt{\mathrm{d}\vec{r}\cdot\mathrm{d}\vec{r}}=\sqrt{\sum_i\left(h_i\mathrm{d}\Omega_i\right)^2}
$$

Similarly, the volume element can be found from the triple product of the components of $\mathrm{d}\vec{r}$
$$
\mathrm{d}V=\mathrm{d}\vec{r}_u\,\vec{\hat{e}_u}\cdot\left(\mathrm{d}\vec{r}_v\,\vec{\hat{e}_v}\times\mathrm{d}\vec{r}_w\,\vec{\hat{e}_w}\right)=h_uh_vh_w\,\mathrm{d}u\,\mathrm{d}v\,\mathrm{d}w\,.
$$

The surface element is given by the magnitude of the cross product
$$
\mathrm{d}S=\lvert\mathrm{d}\vec{r}_u\,\vec{\hat{e}_u}\times\mathrm{d}\vec{r}_v\,\vec{\hat{e}_v}\rvert\,.
$$

<!-- All of these results are an example of a [change of variables](integration-by-substitution.md), and hence the coefficients $h_\Omega$ are the Jacobian -->