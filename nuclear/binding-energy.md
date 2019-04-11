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