Binding Energy
==============
The mass energy $m_Nc^2$ of a nuclide is given in terms of the nuclide's _atomic_ mass energy $m_Ac^2$, the mass energy of its electrons, and their respective binding energies $B_i$:
<!-- Here the mass of the atom excludes the binding energy, so we restore it first before subtracting the isolated electron masses -->
$$
\tag{a}
m_Nc^2 = m_Ac^2+\sum_{i=1}^ZB_i-Zm_ec^2\,.
$$
Conventionally, we neglect the contribution from the electronic binding energies, as they are on the order of $\sim10\operatorname{-}100\,\text{keV}$ vs $ A\times1000\,\text{MeV}$

The _binding energy_ $B$ of the nucleus is the difference in mass energy between the nucleus and its constituent protons and neutrons,
$$
B = \left(Zm_p + Nm_n - \left[m({}^A\text{X})-Zm_e\right]\right)c^2\,.
$$
This expression may be rewritten to use the atomic mass of ${}^1\text{H}$ (which includes the mass of the electrons, but does not reproduce the correct binding energy contribution):
$$
\tag{b}
B = \left(Zm({}^1\text{H}) + Nm_n - m({}^A\text{X})\right)c^2\,.
$$

In order to determine the _atomic_ masses, some tables give the _mass excess_
$$
\tag{c}
\Delta = m({}^A\text{X}) - A\,.
$$
This value is _not_ directly a measure of binding energy, as the mass given by the atomic number is _relative_ to the mass of ${}^{12}\text{C}$.

The binding energy of a nucleus tends to increase linearly with the number of nucleons $A$. The average binding energy per nucleon is approximately $8\,\text{MeV}$. In the figure below, there are two visible regions $A<60$ and $A>60$, in which the specific binding energy increases and decreases respectively. 
![Binding energy per nucleon.](https://upload.wikimedia.org/wikipedia/commons/5/53/Binding_energy_curve_-_common_isotopes.svg)

Separation Energies
-------------------
In addition to binding energy, we can also define the _separation energies_ of protons and neutrons within the nucleus $S_p,\,S_n$
$$
\begin{aligned}
S_p &= B\mathopen{}\left({}^A_Z\text{X}\right)\mathclose{} - B\mathopen{}\left({}_{Z-1}^{A-1}\text{X}\right)\mathclose{}\\
&= \left(m\mathopen{}\left({}^{A-1}_{Z-1}\text{X}\right)\mathclose{}-m\mathopen{}\left({}^A_Z\text{X}\right)\mathclose{}+m\mathopen{}\left({}^1\text{H}\right)\mathclose{}\right)c^2\\ 
&\\
S_n &= B\mathopen{}\left({}^A_Z\text{X}\right)\mathclose{} - B\mathopen{}\left({}_Z^{A-1}\text{X}\right)\mathclose{}\\
&= \left(m\mathopen{}\left({}^{A-1}_Z\text{X}\right)\mathclose{}-m\mathopen{}\left({}^A_Z\text{X}\right)\mathclose{}+m_n\right)c^2\,.
\end{aligned}
$$
If the binding energy increases with removal of a nucleon, it is an energetically favourable process, and thus the separation energy (barrier) is _negative_.

Semi Empirical Mass Formula
---------------------------
### Volume Term
The variation of the binding energy with $A$ of a nucleus can be predicted from the _semi-empirical mass formula_. To the lowest order, $B\propto A$ (given that $\frac{B}{A}\approx 8\,\text{MeV}$), hence we can establish a _volume_ term (as $V\propto A$),
$$
    \tag{a}a_vA\,.
$$
That $B$ depends upon $A$ is interesting, for it implies that the nuclear potential involves a near(est)-neighbour interaction, rather than $A(A-1)$ for all nucleons.

### Surface Term
The volume term over-estimates the contribution to the binding energy of the surface nucleons, which are surrounded by fewer neigbours and hence are less tightly bound than those in the core of the nucleus. A _surface correction_ is therefore required,
$$
    \tag{b}-a_sA^\frac{2}{3}\,.
$$

### Coulomb Repulsion
Let the nuclear radius $R$ be proportional to $A$, 
$$
    R=R_0A^\frac{1}{3}\,.
$$
As protons experience Coulomb repulsion, an additional _repulsive_ term is added to reduce the binding energy
$$
\tag{c}
-\frac{e^2}{2\pi\epsilon_0R_0A^\frac{1}{3}}kZ(Z-1) = -a_cZ(Z-1)A^{-\frac{1}{3}}\,.
$$

### Symmetry
It is observed that stable nuclei have $Z\approx\frac{A}{2}$. An additional _symmetry_ term is required to account for this increase in binding energy,
<!-- TODO motivate form of symmetry expression, mention overlap of orbitals-->
$$
\tag{d}
-a_\text{sym}\frac{(A-2Z)^2}{A}\,.
$$

### Parity
<!-- TODO mention spin coupling -->
A final term is required to account for the tendency of like nucleons to couple pairwise to particularly stable configurations. In the case that the number of protons and neutrons are fully paired ($N$, $Z$ even) there is an _increase_ $\delta_0$ in binding energy. If both $N$ and $Z$ are odd, then there are two nucleons that are unpaired, which minimises the binding energy. The case that $A$ is odd lies in between the other two. Hence,
$$
\tag{e}
\delta=\begin{cases}
    +\delta_0,& \text{M, Z even} \\
    0,              & \text{A odd} \\
    -\delta_0,& \text{M, Z odd} \\
\end{cases}
$$

The final expression for the binding energy $B$ is therefore
$$
\tag{f}
B = a_vA - a_sA^\frac{2}{3} - a_cZ(Z-1)A^{-\frac{1}{3}} - a_\text{sym}\frac{(A-2Z)^2}{A} + \delta\,,
$$

where experimentally the constants have been found as follows
| Constant       	| Experimental Value 	|
|----------------	|--------------------	|
| $a_v$          	| $15.5\,\text{MeV}$ 	|
| $a_s$          	| $16.8\,\text{MeV}$ 	|
| $a_c$          	| $0.72\,\text{MeV}$ 	|
| $a_\text{sym}$ 	| $23\,\text{MeV}$   	|
| $\delta_0$     	| $34\,\text{MeV}$   	|

Using this expression for $B$, we have the _semi-empirical mass formula_
$$
M(Z,A) = Zm\mathopen{}\left({}^1\text{H}\right)\mathclose{} + Nm_n - \frac{B(Z,A)}{c^2}\,.
$$

A plot of $M(Z,A)$ for fixed $A$ shows the decay chain for a given isobar.