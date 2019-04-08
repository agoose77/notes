Inverse Transform Sampling
=============================
Let $F_X:\mathbb{X}\rightarrow[0,1]$ be the CDF of some random variable $X$. Given that $F_X\in[0,1]$, we may take some $U\sim \operatorname{Uniform}[0, 1]$ to randomly sample from $X$ using its CDF. The method is as follows:
1. Generate a random number $u$ from $U\sim\operatorname{Uniform}[0, 1]$.
1. Find the inverse CDF of $X$, $F_X^{-1}$.
1. Compute $X=F_X^{-1}(u)$. $X$ will be distributed under the CDF $F_X$.


Uniform Spherical Polar Coordinates
-----------------------------------
Let $f(\vec{r})$ be a probability density function, such that
$$
\begin{array}{cc}
\iint\limits_Sf(\vec{r})\,\mathrm{d}s=1\,, & \iint\limits_S\,\mathrm{d}S=4\pi\,.
\end{array}
$$

Then $f(\vec{r})\,\mathrm{d}S$ is the probability of finding a point in $\mathrm{d}S$ about $\vec{r}$. For a uniform distribution on $S$, $f(\vec{r}) = k=\frac{1}{4\pi}\,\forall\,\vec{r}$. 

Let us now consider the equivalent distribution $f(\theta,\phi)$ in spherical polar coordinates. In this parameterisation, the probability of finding a point in $\mathrm{d}\theta\,\mathrm{d}\phi$ about $(\theta, \phi)$ is $f(\theta,\phi)\,\mathrm{d}\theta\,\mathrm{d}\phi$. Note that we do not simply transform from the Cartesian basis; we are interested in the _distribution function_ in the $\theta,\,\phi$ parameter space.

Hence, equating the two probaiblities, it follows that $f(\vec{r})\,\mathrm{d}S = f(\theta, \phi)\,\mathrm{d}\theta\,\mathrm{d}\phi$. Given that $f(\vec{r})=\frac{1}{4\pi}$, it follows that 
$$
\frac{1}{4\pi}\sin(\phi)\,\mathrm{d}\theta\,\mathrm{d}\phi = f(\theta, \phi)\,\mathrm{d}\theta\,\mathrm{d}\phi\,,
$$
hence $f(\theta, \phi)=\frac{\sin(\phi)}{4\pi}$.

Let us now _marginalise_ the joint distribution $f(\theta,\phi)$, and find the PDF of $\theta$ and $\phi$ separately. For continuous random variables, the marginal probability density function can be written as 
$$
    p_X(x) = \int_y p_{X,Y}(x,y)\,\mathrm{d}y = \int_y p_{X|Y}(x|y)p_Y(y)\,\mathrm{d}y\,,
$$
hence we find $f(\theta)$ and $f(\phi)$ as follows:
$$
\begin{aligned}
f(\theta) &= \int_0^\pi f(\theta,\phi)\,\mathrm{d}\theta=\frac{1}{2\pi}\\
f(\phi) &= \int_0^{2\pi} f(\theta,\phi)\,\mathrm{d}\phi=\frac{\sin(\phi)}{2}\,.
\end{aligned}
$$

Now, to sample from $f(\theta, \phi)$, we use Inverse Transform Sampling. Let 
$$
    F(\theta)=\int_0^\theta f(\theta)\,\mathrm{d}\theta=\frac{1}{2\pi}\int_0^\theta\,\mathrm{d}\theta\,.
$$
Given that $F(\theta)$ is the CDF of $\theta$, and the _inverse_ CDF is defined to bedistributed uniformly, then $\theta=2\pi F(\theta)=2\pi v$ where $V\sim\operatorname{Uniform}[0, 1]$. 

Similarly, for $\phi$,
$$
 F(\phi)=\int_0^\phi f(\phi)\,\mathrm{d}\theta=\int_0^\phi\frac{\sin(\phi)}{2}\,\mathrm{d}\phi=\frac{-\cos(\phi)}{2}\Bigg|_0^\phi\,.
$$
Solving for $\phi$, we find that
$$
\phi=\cos^{-1}(1-2\mu)\,
$$
where $\mu\sim\operatorname{Uniform}[0, 1]$. 