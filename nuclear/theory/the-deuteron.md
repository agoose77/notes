# The Deuteron

A deuteron $\atom{2}{H}$ is the simplest bound state of nucleons, consisting of a proton and neutron. A neutral atom of $\atom{2}{H}$ is called _deuterium_. As a weakly bound system, it has no excited states; the only excited states are unbound systems (that of a free proton and neutron).

## Binding Energy

The [binding energy](binding-energy.md#Binding-Energy) of the deuteron is precisely known, using techniques such as [the mass doublet method](binding-energy.md#Mass-Doublet-Method), which gives[^krane]

$$
\tag{a}
m(\text{C}_6\text{H}_{12})- m(\text{C}_6\text{D}_{6}) = (9.289710 \pm 0.000024)\times 10^{-3}\unit{\amu}\,.
$$

From **(a)**, it follows that $m(\atom{2}{D}) = 2.014101789 \pm 0.000000021\unit{\amu}$. The binding energy is then 
$$
B = \left[m(\atom{1}{H}) + m(n)-m(\atom{2}{H})\right]c^2 = 2.22463\pm 0.0004 \unit{\MeV}\,.
$$
One can also determine the binding energy by bringing together an unbound proton and neutron together to form $\atom{2}{H}$, and measuring the energy of the photon emitted (plus a recoil correction):
$$
    \atom{1}{H} + n \rightarrow \atom{2}{H} + \gamma\,.
$$
This reaction can be performed in reverse; determining the minimum photon energy required to produce deuterium (less the recoil energy).

Given that the average binding energy per nucleon [is about $8\unit{\MeV}$](binding-energy.md#Binding-Energy), it follows that the deuteron is very weakly bound in comparison to typical nuclei.
<!--
TODO only if we write up spherical potential to justify \psi=u(r)/r
We might model the nucleon-nucleon potential of the deuteron as a simple three-dimensional square well:

![Idealised spherical square well potential of the deuteron](images/binding-energy-deuteron.png)

expressed in equation form as
$$
V(r) = \begin{cases}
-V_0, & r \leq R\\
0, & r > R\\
\end{cases}\,.
$$
Given that $r$ represents the separation of the neutrons, $R$ is effectively a measure of the diameter of the deuteron.

Also vaguely relevant - https://ocw.mit.edu/courses/nuclear-engineering/22-02-introduction-to-applied-nuclear-physics-spring-2012/lecture-notes/MIT22_02S12_lec_ch5.pdf
-->

Spin and Parity
---------------
$\gdef\S{\hat{S}}$
The total angular momentum $I$ of the deuteron is given by the sum of the angular momenta of the nucleons, which add according to a set of [addition rules](../../quantum-mechanics/angular-momentum-addition.md). We can consider the total angular momentum $\hat{I}$ as
$$
\vb{\hat{I}} = \vb{\hat{L}}_1 + \vb{\S}_1 + \vb{\hat{L}}_1 + \vb{\S}_1\,.
$$
It is conventional to consider the addition of the orbital angular momentum of the entire system and the individual spins:
$$
\tag{b}
\vb{\hat{I}} = \vb{\hat{L}} + \vb{\S}_1 + \vb{\S}_1\,,
$$
though one could also express $I$ in terms of the total orbital and spin operators
$$
\vb{\hat{I}} = \vb{\hat{L}} + \vb{\S}\,.
$$
From [addition of the two spins](../../quantum-mechanics/two-particle-spin-half-states.md), the total spin $S$ has a singlet state $\ket{s=0;m_s=0}$ and a triplet state $\ket{s=1;m_s=\pm 1,0}$
In nature, the deuteron is observed to have $I=1$. We may determine which states couple to produce $I=1$, given that $S\in\set{0,\,1}$ and $L\geq 0$:

| $l$ 	| $s$ 	| $\set{I}$         	|
|:---:	|:---:	|-------------------	|
|  0  	|  0  	| $\set{0}$         	|
|  0  	|  1  	| $\set{1}$         	|
|  1  	|  0  	| $\set{1}$         	|
| 1   	| 1   	| $\set{0,\,1,\,2}$ 	|
| 2   	| 0   	| $\set{2}$         	|
| 2   	| 1   	| $\set{1,\,2}$     	|

It can be seen that there are four ways to couple $L$ and $S$ to produce $I=1$. In order to identify states which the deuteron can occupy, it suffices to look at the parity of the deuteron wavefunction, which experimentally is found to be even. To determine the parity of these states, let us first consider how the parity of a state ket $\ket{\alpha}$ affects the wavefunction $\psi$. If 
$$
\psi(\vb{x}') = \braket{\vb{x}'}{\alpha}
$$
Then under parity, the wavefunction becomes
$\gdef\parity{\hat{\pi}}$
$$
\begin{aligned}
\psi(-\vb{x}') 
&= \bra{\vb{x}'}\parity\ket{\alpha}\\
&= \braket{-\vb{x}'}{\alpha}\,.
\end{aligned}
$$
To have even parity, the state ket $\alpha$ must be an eigenket of $\parity$ (to have definite parity) with an eigenvalue of $+1$. We can express a state ket as
$$
\ket{\alpha} = \ket{\alpha_\vb{r}}\otimes\ket{\alpha_\vb{S}}\,.
$$
<!-- TODO: is this definition of parity (i.e. only acts on position space) valid? : http://www.pas.rochester.edu/~passage/resources/prelim/Quantum/UCB%20Notes/19%20parity.pdf -->
Evidently, the parity of the wavefunction depends solely upon the position ket, as
$$
\parity = \parity_\vb{r}\otimes1_\vb{S}\,,
$$
which gives
$$
\begin{aligned}
\bra{\vb{x}}\parity\ket{\alpha}
&= \left(\bra{\vb{x}}\otimes 1\right)\left[\parity_\vb{r}\otimes1_\vb{S}\right]\left(\ket{\alpha_\vb{r}}\otimes\ket{\alpha_S}\right)\\
&= \bra{\vb{x}}\parity_\vb{r}\ket{\alpha_\vb{r}}\otimes\ket{\alpha_\vb{S}}\\
&= \psi_\vb{r}\ket{\alpha_\vb{S}}\,.
\end{aligned}
$$
We can express the position ket in the [eigenbasis of the orbital angular momentum operators](../../quantum-mechanics/orbital-angular-momentum.md) $\L_z$ and $\L^2$:
$$
\ket{\alpha_\vb{r}} = \sum_l\sum_{m_l}^{2l+1}\sum_k^{N(l)} \ket{k,l,m_l}\overline{R_{l,k}(r')Y_l^{m_l}\mleftright{(}{\theta',\phi'}{)}}\,.
$$
An orbital angular momentum wavefunction has a parity defined by 
$$
\pi \ket{k,l, m_l}=(-1)^{l} \ket{k,l,m_l}\,,
$$
which follows from the fact that behaviour of the spherical harmonics under parity
$$
\begin{aligned}
\bra{\vb{x}'}\hat\pi\ket{k,l,m_l} 
&= \braket{-\vb{x}'}{k,l,m_l}\\
&= (-1)^l\braket{\vb{x}'}{k,l,m_l}\\
&= \bra{\vb{x}'}(-1)^l\ket{k,l,m_l}\,.
\end{aligned}
$$
It is clear that $R_{l,k}$ is invariant under parity, as $r$ is unchanged.
Hence, for the parity of $\ket{\alpha_\vb{r}}$ to be even, i.e.
$$
\braket{\vb{x}}{\alpha} = \braket{-\vb{x}}{\alpha}\,,
$$
we require that
$$
\psi_\vb{r}(\vb{x}')\ket{\alpha_\vb{S}} = \psi_\vb{r}(-\vb{x}')\ket{\alpha_\vb{S}}\,.
$$
In the angular momentum basis, $\bra{\vb{x}'}\parity\ket{\alpha_\vb{r}}$ is 
$$
\begin{aligned}
\bra{\vb{x}'}\parity\ket{\alpha_\vb{r}} 
&= \sum_l\sum_{m_l}^{2l+1}\sum_k^{N(l)} \bra{\vb{x}'}\parity\ket{k,l,m_l}\overline{R_{l,k}(r')Y_l^{m_l}\mleftright{(}{\theta',\phi'}{)}}\\
&= \sum_l\sum_{m_l}^{2l+1}\sum_k^{N(l)} (-1)^{l} \braket{\vb{x}'}{k,l,m_l}\overline{R_{l,k}(r')Y_l^{m_l}\mleftright{(}{\theta',\phi'}{)}}\,.
\end{aligned}
$$
As $\ket{\alpha_\vb{r}}$ is a sum of states with distinct parities, it follows that for $\psi(\vb{x}')=\psi(-\vb{x}')$ only the even parity contributions to the expansion in $\ket{k,l,m_l}$ are permitted, i.e.
$$
l \in 2\mathbb{N}\,.
$$

This leaves only the $l=0$ and $l=2$ states from the above table.


Magnetic Dipole Moment
----------------------
It [was observed](electromagnetic-moments.md) that there are both spin and orbital angular momentum contributions to the magnetic *dipole* moment of the nucleus, according to the values of $l$ and $s$. With $l=0$, there will be solely a spin contribution
$$
\def\mom{\vb{\mu}}
\begin{aligned}
\mom 
&= \mom_n + \mom_p\\
&= \frac{g_\text{sn}\mom_N}{\hbar}\vb{s}_n + \frac{g_\text{sp}\mom_N}{\hbar}\vb{s}_p\\
\end{aligned}
$$
Taking the observed magnetic moment to be that when the spin $z$ projections $m_z\hbar$ have their maximum projection, it follows that
$$
\begin{aligned}
\mu 
&= \frac{1}{2}\mu_N\left(g_\text{sn}+g_\text{sp}\right)\\
&= 0.879804\operatorname{\mu_N}\,.
\end{aligned}
$$
Experimentally, the observed value is $0.7574376 \pm 4\times 10^{-7}\operatorname{\mu_N}$, which does not agree with this calculation. Though this discrepancy can be attributed to several factors including contributions from the mesons exchanged between the nucleons, it can be assumed that a contribution to $\mu$ from the *orbital angular momentum* is its primary origin. Let the deuteron have its state ket defined by
$$
\alpha\ket{l=0}\otimes\ket{s=1} + \beta\ket{l=2}\otimes\ket{s=1}
$$
<!-- TODO analysis of this mixture must come from form of dipole moment of nucleus. 
https://en.wikipedia.org/wiki/Nuclear_magnetic_moment
Samuel Wong: p.6
-->
<!-- TODO discuss the fact that l=0 predicts vanishing quadrupole moment (see electromagnetic-moments.md), yet we observe nonzero positive Q=0.00288 \pm 0.00002\barn which implies l=0 + l=2. Therefore the deuteron is non-spherical. This means that the n-p potential is non central-is a tensor. dV/d0 =/= 0, so there is a force -> torque -> L not conserved
-->
<!-- TODO 
The
orbital angular momentum is, therefore, not a good quantum number and the nucleon-
nucleon interaction potential does not, commute with the operator L^2 [(why?)]:
...
The fact that the deuteron ground state is a linear combination of these two
basis states implies that the off-diagonal matrix elements are not zero
-->
[^wong.62]: Samuel S. M. Wong, Introductory Nuclear Physics, 2. ed. ed. (Wiley, New York [u.a.], 1998), p. 64.
[^krane]: Kenneth S. Krane, Introductory nuclear physics, (Wiley, New York u.a, 1987), p. 81.