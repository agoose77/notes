Cross Section
=============

The (mutual) *cross section* $\sigma$ of two interacting particles is the area transverse to their relative motion[^transverse] within which they must meet in order to scatter from one another.

If we consider a medium containing target particles of number density $n_t$, then the number of particles encountered by the incident particle in the length $T$ is
$$
\tag{1}
N = n_tAT\,.
$$
The interaction probability $P$ is given by the ratio of the effective target area $N\sigma$ to the incident particle area $A$,
$$
P = \frac{n_tAT\sigma}{A} = n_t\sigma T\,.
$$
Often, one does not measure $\sigma$ directly, but instead the *differential* cross section $\dd\sigma$ through a differential region $\dd\Omega$.
It follows from **(1)** that the probability density function with respect to solid angle for scattering through some angle $(\theta, \phi)$ is given by
$$
P(\theta,\phi) = \dv{\sigma}{\Omega}nT\,.
$$
The *total cross section* $\sigma$ is simply the integral over the the unit sphere
$$
\tag{2}
\int_S \dv{\sigma}{\Omega} \dd\Omega\,.
$$
In spherical polar coordinates, **(2)** becomes
$$
\int_0^{2\pi}\int_0^{pi}\dv{\sigma}{\Omega}\sin(\theta)\dd\phi\dd\omega\,.
$$

[^transverse]: The area in the plane whose normal lies along the motion vector.