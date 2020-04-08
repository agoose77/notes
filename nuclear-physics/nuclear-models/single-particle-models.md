Single Particle Models
======================

Choosing a Many-Body Basis
-------------------------
### Direct Product Basis
The states of a nucleus can be described in terms of the $N$ single-particle *nucleon* degrees of freedom. In order to do so, one may choose the set of many-body basis states $\set{\ket{\psi_i}}$ as direct products $\ket{\psi_i}\in V\otimes V \otimes \dots \otimes V$ of individual nucleon states $\ket{\phi_j}\in V$. 
Each single-particle state $\ket{\phi_j}$ is an eigentstate of the single-particle Hamiltonian $\hat{H}^0$:
$$
\hat{H}^0 \ket{\phi_j} = \epsilon^0_j \ket{\phi_j}\,.
$$
The many-body states are written as
$$
\ket{\psi_{j_1,j_2,\dots,j_N}} = \ket{\phi_{j_1}, \phi_{j_2}, \dots,\phi_{j_N}} = \ket{\phi_{j_1}}^{(1)}\otimes\ket{\phi_{j_2}}^{(2)}\otimes\dots\otimes\ket{\phi_{j_N}}^{(N)}\,,
$$
where $\ket{\phi_{j_k}}^{(k)}$ corresponds to particle $k$ in the single-particle state $\ket{\phi_{j_k}}$, i.e. each many-body state is parameterised by the indices $\begin{pmatrix}j_1 & j_2 & \dots & j_N\end{pmatrix}$. The particle index ${}^{(j)}$ can be taken implicitly from the position within the product.

A general many-body wavefunction may be expanded in terms of these basis states:
$$
\ket{\psi_a} = \sum_i \alpha_i \ket{\psi_i}\,.
$$
Evidently, it will not always be possible to represent $\ket{\psi_a}$ as a single direct product state. In such cases, the states are *entangled*.[^mit.quantum-ii]

The Hamiltonian on this many body basis behaves as
$$
\begin{aligned}
\hat{H} 
&= \pqty{\hat{H^0_1}\otimes \mathbf{1} \otimes \mathbf{1} \dots} + \pqty{\mathbf{1} \otimes \hat{H^0_2}\otimes \mathbf{1} \dots} + \dots +  \hat{\tilde{V}} \\
&= \pqty{\hat{H^0_1}\otimes \hat{H^0_2} \otimes \dots \hat{H^0_N}} + \hat{\tilde{V}}\,,
\end{aligned}
$$
where $\hat{\tilde{V}}$ is the residual interaction describing the remaining contribution to the Hamiltonian from two body interactions which is not included in the single particle hamiltonians.
Equivalently, one may write:[^jbrader.many-body]
$$
\tag{a}
\hat{H} = \sum_i^N \hat{H^0_n} + \sum_{i>j}\hat{\tilde{V_{ij}}}\,,
$$
where $\hat{H^0_i}$ is the single-particle Hamiltonian acting on particle $i$ in the many body space, e.g. 
$$
\begin{aligned}
    \hat{H^0_0}&=\hat{H^0}\otimes\mathbf{1}\otimes\dots\\
    \hat{H^0_1}&=\mathbf{1}\otimes\hat{H^0}\otimes\dots\\
    &\;\;\vdots\\
    \hat{H^0_N}&=\dots\otimes\mathbf{1}\otimes\hat{H^0}\,,
\end{aligned}
$$
and $\hat{\tilde{V_{ij}}}$ the residual interaction operator acting on particles $i,\,j$ in the many body space. N.b. $i>j$ ensures that we count each interaction $i,\,j$ only once, assuming commutativity.

### Antisymmetrised Basis
Under exchange, nucleons behave as fermions, which requires that the wavefunction of the system be anti-symmetric w.r.t. exchange. Consequently, a better choice of basis for the many-body system would be a set of anti-symmetric many-body states. A subset of these are given by the Slater determinant
$$
\begin{aligned}
    \tag{b}
    \ket{\psi_A}
    &= \frac{1}{\sqrt{N!}}\begin{vmatrix}
        \ket{\phi_{j_1}}^{(1)} & \ket{\phi_{j_1}}^{(2)} & \dots  & \ket{\phi_{j_1}}^{(N)} \\
        \ket{\phi_{j_2}}^{(1)} & \ket{\phi_{j_2}}^{(2)} & \dots  & \ket{\phi_{j_2}}^{(N)} \\
        \vdots & \vdots & \ddots & \vdots \\
        \ket{\phi_{j_N}}^{(1)} & \ket{\phi_{j_N}}^{(2)} & \dots  & \ket{\phi_{j_N}}^{(N)} \\
    \end{vmatrix}\\
    &= \mathcal{A}\Bqty{\phi_1, \phi_2, \dots, \phi_N}\,.
\end{aligned}
$$
For a simple two particle system, the Slater determinant given in **(b)** is
$$
\begin{aligned}
    \ket{\psi_A}
    &= \frac{1}{\sqrt{2!}}\begin{vmatrix}
        \ket{\phi_{j_1}}^{(1)} & \ket{\phi_{j_1}}^{(2)}\\
        \ket{\phi_{j_2}}^{(1)} & \ket{\phi_{j_2}}^{(2)} \\
    \end{vmatrix}\\
    &= \frac{1}{\sqrt{2!}}\pqty{\ket{\phi_{j_1}}\otimes \ket{\phi_{j_2}}-\ket{\phi_{j_2}}\otimes\ket{\phi_{j_1}}}\,.
\end{aligned}
$$

<!-- TODO see [^slater.condon] on the F and G operators which seem like the mean field and residual components of the many body hamiltonian -->

Determining Single Particle States
----------------------------------
From **(a)** it is clear that one can choose a single-particle Hamiltonian such that the residual interaction $\hat{\tilde{V}}$ is minimised. To solve the many-body problem, it follows that there are two main approaches:
* Choose $\hat{H^0}$ (i.e. choose $\ket{\phi_i}$) to minimise the residual interaction such that it can be ignored - the independent particle model.
* Choose a reduced subspace of many body wavefunctions within which an *effective* residual interaction may be defined - the (spherical) shell model.

### Hartree Fock
#### Variational Principle
<!-- [^isacker.structure]:
Hartree-Fock-Bogoliubov (HFB): Includes pairing
correlations in mean-field treatment.
Tamm-Dancoff approximation (TDA):
Ground state: closed-shell HF configuration
Excited states: mixed 1p-1h configurations
--> 
<!-- [^wong]
[given] that the two-body interaction between nucleons is fairly strong, it is not easy in general to truncate the Hilbert space involved down to sizes suitable for practical calculations.[i.e. need many states in basis?]

One of the aims of the Hartree-Pock approach to the nuclear many-body problem is to find a single-particle representation such that the residual interaction is small
-->
<!-- [^rowe.collective] p.142
HF gives ground state, and excited states can be treated with 1p1h excitations (TDA)

---
the interaction has an infinite (or, at least, very strong) repulsive core at a distance .-.0-4 fm. Why is this disastrous for the HF method? Because relative wave functions, for independent particles, inevitably penetrate the core. Matrix elements of the interaction are therefore infinite and the particles may be expected to scatter far and wide out of their HF orbitals.
::
> scatter far and wide
implies that we would have elements in the interaction matrix that connect very energetically distant states -> can't use small basis. For reduced basis, need an *effective* interaction
-->
<!-- [^rowe.collective] p. 145
IPaM (Independent Pair Model).
In this model it is assumed that the relative motion of two particles, in a Fermi sea (states below fermi surface), is influenced by the rest of the particles only via the self-consistent field* and the Pauli principle

[of residual interaction]:
In particular they are restrained from scattering particles within the Fermi sea, just because there are no available unoccupied states for them to scatter into.
The residual interactions are not restrained, however, from scattering particles out of the Fermi sea, although VI is not strong enough to lift particles far above the surface. The effect is to bring about a diffuseness of the Fermi surface. The corresponding admixtures into the HF wave function are described generally as ground-state correlations. Thus there are pair correlations, due to the residual interaction in addition to the hard core correlations of the IPaM.
-->

<!-- 
For the ground state of a closed-shell nucleus, the shell model is simply a first approximation to HF theory. For nuclei with particles outside a closed shell, the conventional shell model is no longer an approximation to HF theory. Its method is to set up a basis of wave functions by putting the valence particles into the various unoccupied levels of the unperturbed closed-shell core. The two-body interaction is then introduced explicitly and diagonalized within this configur- ation space. By eliminating the core in this way, that is by taking it into account only via the exclusion principle and the potential well it generates, the shell model reduces the many-body problem to a few- body problem. For two or three valence particles this works very well.
-->

<!-- TODO:
* Is it the EIPM or IPM that lets V~ = 0?
* Clarify that the form of (a) originates from H = T + V, let U = T + V_onebody -> H = U + (V - V_onebody) = U + V~. See slide 6. [^isacker.structure]
  * The anti-symmetrised basis is equally fine for classic H = T + V. We only later let H = U + V~ in order to choose U such that V~ becomes negligible, or small enough to treat (use) on the new basis. S
* See Jelley 8.6 F.o.N.P on use of diagonalising V~ in shell model basis
-->

[^krane.74]: Kenneth S. Krane, Introductory nuclear physics, (Wiley, New York u.a, 1987), p. 74.
[^slater.condon]: https://booksite.elsevier.com/9780444594365/downloads/16755_10033.pdf
[^mit.quantum-ii]: https://ocw.mit.edu/courses/physics/8-05-quantum-physics-ii-fall-2013/lecture-notes/MIT8_05F13_Chap_08.pdf
[^jbrader.many-body]: https://theorie.physik.uni-konstanz.de/jbrader/Many_body.pdf
[^isacker.structure]: http://indico.ictp.it/event/a13191/session/0/contribution/4/material/0/0.pdf