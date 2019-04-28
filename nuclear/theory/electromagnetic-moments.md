Electromagnetic Moments
=======================
Whilst it is the [strong force](strong-force.md) which establishes the motion and distribution of the nucleons within the nucleus, one can use the electromagnetic interaction to prove these properties. A far weaker force, the electromagnetic interaction can perform measurements of the nucleus without significantly distorting the object under measurement. Concerning the *distribution* of the nucleons within the nucleus, one can use multipole theory (analogous to that of [classical electromagnetic theory](../../electromagnetism/multipole-expansion.md)) to investigate the electromagnetic moments of the nucleus. The moments in the classical theory correspond to operators in the quantum mechanical reigime, whose expectation values yield the quantity of interest.

* ~~Electric and magnetic multipole theory applies to nuclear reigime using QM~~
* Each EM moment has an associated parity, given by behaviour of multipole operator under parity.
  * Parity of electric moment is $(-1)^l$
  * Parity of magnetic moment is $(-1)^{l+1}$
* When computing the expectation value of a moment, *odd parity moments* will hence vanish, so we have the electric mono + quadrupoles, magnetic dipole, etc...
* In QM we _operationally define_ the observable magnetic moment greatest component of $\mu$ to the direction of the greatest component of $l$. ##
* Monopole E just Ze
* Dipole moment $\mu$ given by $\frac{e}{2m}\abs{l_i}$, where max $m$ is given by $m_l=l$, so $\abs{l_i}=l\hbar$. $\frac{e\hbar}{2m}$ is called a magneton. Using the electron mass gives you Bohr magneton. Using proton mass gives Nuclear Magneton. $\mu_N\ll \mu_B$, hence atomic effects greater than nuclear. $\mu=g_ll\mu_N$ is another form for $\mu$. $g_l$ is 0 for neutrons (uncharged) and $1$ for protons. This is just *orbital* angular momentum. A similar relation exists for spin $\mu=g_ss\mu_N$. For spin half, $g_s=2$ (according to dirac eqn). Experimentally, it's measured to be be 2.0023. For free nucleons, however, experiment and theory differ significantly. In particular, the uncharged neutron has a nonzero moment, which implies the existence of internal structure with charged particles in motion, whose currents give the observed moments. Interestingly the differences between expt and theory are equal in both cases. Adding the magnetic moments of the component quarks yields the experimental values directly.
* The paired off nucleons thus have no total magnetic moment contribution, hence only valence electrons do.
* quadrupole moment is next nonvanishing - show how 3Q vanishes https://physics.stackexchange.com/questions/401007/does-the-electric-quadrupole-vanish-if-psi2-is-spherically-symmetric
 If $\phi$ is spherically symmetric, then it is invariant under rotation. Hence, for each coordinate $$
 \begin{aligned}
 \tag{a}
Q 
& = \int(3z^2-r^2)|\psi(\mathbf r)|^2 \mathrm d^3\mathbf r
\\& = \int(3y^2-r^2)|\psi(\mathbf r)|^2 \mathrm d^3\mathbf r
\\& = \int(3x^2-r^2)|\psi(\mathbf r)|^2 \mathrm d^3\mathbf r.
 \end{aligned}
$$
Thus, it follows that $$
 \begin{aligned}
3Q 
& = \int(3(x^2+y^2+z^2)-3r^2)|\psi(\mathbf r)|^2 \mathrm d^3\mathbf r
\\ & = \int(3r^2-3r^2)|\psi(\mathbf r)|^2 \mathrm d^3\mathbf r
\\ & = 0
 \end{aligned}
$$
Simplisticly, for a particle confined to the $xy$ plane, it follows that $z\approx 0$, and hence **(a)** becomes $\int_{V'}\overline{\psi}-r^2\psi\dd \vb{V'}$, i.e. $-\expval{r^2}$. Similarly, when confined to the $z$ axis (i.e. $x\approx y\approx 0$), it follows that $z=r$ and thus **(a)** becomes $\int_{V'}\overline{\psi}2r^2\psi\dd \vb{V'}$, i.e. $2\expval{r^2}$, twice the mean-square-radius of the orbit.
Given the assumption that paired off nucleons have spherically symmetric orbits, [TODO why assume this?], then their contribution to $Q$ is zero, and thus only the valence nucleon affects the quadrupole moment. Hence, we would expect small $Q$ values. Several rare-earth nuclei have $Q$ values far beyond these predicted values. This implies a deformed nucleus, with contributions from most of the nucleons to $Q$. 