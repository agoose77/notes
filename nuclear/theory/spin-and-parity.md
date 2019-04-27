$\gdef\I{\hat{I}}$
Spin and Parity
===============
The total angular momentum operator on the vector space formed from the tensor product of the $n$ nucleon states [can be shown](../../quantum-mechanics/angular-momentum-addition.md) to behave as an angular momentum. This angular momentum, that of the entire nucleus, is called the _nuclear spin_, represented by the symbol $I$. As an _angular momentum_, we may therefore represent the momentum state of the entire nucleus through two quantum numbers $I$ and $m$.

In ordinary magnetic fields, we can observe the _nuclear_ Zeeman effect, as the state $I$ splits into $2I+1$ equally spaced substates. If one could apply an incredibly strong magnetic field, it would be possible to see the individual $j$ splitting of each nucleon, but no such fields can be produced. Hence, we observe the nucleus as though it were a single spinning particle.

It is observed that fermions _half-integer_ spin, and that the _orbital_ angular momentum $l$ must be integer. Thus, by the rules of angular momentum addition, nucleons must have half-integeral spin. Given that successive values of $I$ are separated by integer steps of $\hbar$, it therefore follows that the nucleus will have integer or half integer spin $I$, depending upon whether $A$ is odd or even, as

$$
\begin{aligned}
m_\text{nucleus} &= m_1 + m_2 + \dots + m_A\\
I_\text{max} &= m_\text{max}\,.
\end{aligned}
$$

Furthermore, it is observed that all even-$Z$ even-$N$ nuclei have spin-$0$ ground states. This provides evidence for the nuclear pairing force term in the [semi empirical mass formula](binding-energy.md#Parity), as the nucleons couple in pairs to spin-$0$ (both $l$ and $s$)[^1], leaving $I=0$. In addition, odd-$A$ nuclei therefore must behave $I$ equal to the $j$ of the odd proton or neutron.<!-- TODO is this spin-0 SPIN or TOTAL ang-mom for the nucleons? -->
In addition to nuclear spin, the [parity](../../quantum-mechanics/parity.md) is also used to label nuclear states, in the form $I^\pi$ e.g. $I^-$ or $I^+$.

<!-- TODO
If the wavefunction corresponds to an eigenstate of parity, then it has _definite parity_. Hence, if all nucleons satisfy this property, and it can be shown that the wavefunctions can be multiplied to give the w.f. of the nucleus, then it follows that under parity, there will be definite even/odd parity of nucleus?
-->

<!-- 
* Electric and magnetic multipole theory applies to nuclear reigime using QM
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

--> <!-- p73 ## -->

[^1]: Introductory Nuclear Physics, Krane, p. 74.
