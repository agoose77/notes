Binding Energy
==============

The mass energy $m_Nc^2$ of a nuclide is given in terms of the nuclide's _atomic_ mass energy $m_Ac^2$, the mass energy of its electrons, and their respective binding energies $B_i$:

<!-- Here the mass of the atom excludes the binding energy, so we restore it first before subtracting the isolated electron masses -->

$$
\tag{a}
m_Nc^2 = m_Ac^2+\sum_{i=1}^ZB_i-Zm_ec^2\,.
$$

Conventionally, we neglect the contribution from the electronic binding energies, as they are on the order of $\sim10\operatorname{-}100\unit{\keV}$ vs $ A\times1000\unit{\MeV}$

The _binding energy_ $B$ of the nucleus is the difference in mass energy between the nucleus and its constituent protons and neutrons,

$$
B = \left(Zm_p + Nm_n - \left[m(\atom{A}{X})-Zm_e\right]\right)c^2\,.
$$

This expression may be rewritten to use the atomic mass of $\atom{1}{H}$.

$$
\tag{b}
B = \left(Zm(\atom{1}{H}) + Nm_n - m(\atom{A}{X})\right)c^2\,.
$$
Although the electron binding energy contribution is not reproduced correctly, this is negligible. In order to determine the _atomic_ masses, some tables give the [mass excess](nuclear-masses.md#Mass-Excess).


$\gdef\BpA{\overline{B_A}}$
The binding energy of a nucleus tends to increase linearly with the number of nucleons $A$. The average binding energy per nucleon $\BpA$ is approximately $8\unit{\MeV}$. In the figure below of the specific binding energy for the most stable member of each [isobar](basic-concepts.md), there are two visible regions $A<60$ and $A>60$, in which the binding energy increases and decreases respectively.
![Binding energy per nucleon.](https://upload.wikimedia.org/wikipedia/commons/5/53/Binding_energy_curve_-_common_isotopes.svg)

$\alpha$ Clustering
-------------------
<!-- TODO define valley of stability -->
<!-- TODO justify this behaviour -->
The sharp increase in $\BpA$ for small $A$ derives from the increasing number of nucleon pairs.[^wong.10-11] Visible in the above figure are a number of discrete jumps for $A=4n:n\in \mathbb{N}$ nuclei. In the low mass region, the valley of stability corresponds to $N=Z$, so these $4n$ nuclei can be considered as composed of $\alpha$ particles. Given that $\BpA(4n\pm 1) < \overline{B}_A(4n)$, it follows that there might exist $\alpha$-particle clusters which preferentially form in light nuclei. By taking the difference
$$
\tag{4}
\Delta B = B(N,Z) - nB(\atom{4}{He})\,,
$$
we can approximately determine the total interaction energy between these clusters. Dividing **(4)** by the number of alpha particle pairs $n(n-1)/2$[^pairs], it can be shown that the inter-cluster binding energy is around $2\unit{\MeV}$. The property that the nuclear force is strongest between the nucleons of a group of $2p,2n$, i.e. the preferential formation of $\alpha$-particle clusters in nuclei, is known as the "saturation of nuclear force."[^wong.10-11]
> It is a reflection of a fundamental symmetry of nuclear
force, known as SU4 or Wigner supermultiplet symmetry[^wong.10-11]

Separation Energies
-------------------

In addition to binding energy, we can also define the _separation energies_ of protons and neutrons within the nucleus $S_p,\,S_n$

$$
\begin{aligned}
S_p &= B\mathopen{}\left({}^A_Z\text{X}\right)\mathclose{} - B\mathopen{}\left(\nucleus{Z-1}{A-1}{X}\right)\mathclose{}\\
&= \left(m\mathopen{}\left(\nucleus{A-1}{Z-1}{X}\right)\mathclose{}-m\mathopen{}\left(\nucleus{A}{Z}{X}\right)\mathclose{}+m\mathopen{}\left(\atom{1}{H}\right)\mathclose{}\right)c^2\\
&\\
S_n &= B\mathopen{}\left(\nucleus{A}{Z}{X}\right)\mathclose{} - B\mathopen{}\left(\nucleus{Z}{A-1}{X}\right)\mathclose{}\\
&= \left(m\mathopen{}\left({}^{A-1}_Z\text{X}\right)\mathclose{}-m\mathopen{}\left({}^A_Z\text{X}\right)\mathclose{}+m_n\right)c^2\,.
\end{aligned}
$$

If the binding energy increases with removal of a nucleon, it is an energetically favourable process, and thus the separation energy (barrier) is _negative_.


[^wong.10-11]: Samuel S. M. Wong, Introductory Nuclear Physics, 2. ed. ed. (Wiley, New York [u.a.], 1998), pp. 10-11.
[^pairs]: $n(n-1)$ gives the number of unique pairs $(\alpha_i, \alpha_J)\neq (\alpha_j,\alpha_i)$, hence we divide by a factor of two to eliminate this double counting.