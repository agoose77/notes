The Deuteron
============
A deuteron $\atom{2}{H}$ is the simplest bound state of nucleons, consisting of a proton and neutron. A neutral atom of $\atom{2}{H}$ is called *deuterium*. As a weakly bound system, it has no excited states; the only excited states are unbound systems (that of a free proton and neutron).

Binding Energy
--------------
The [binding energy](binding-energy.md#Binding-Energy) of the deuteron is precisely known, using techniques such as [the mass doublet method](binding-energy.md#Mass-Doublet-Method), which gives[^1]
$$
\tag{a}
m(\text{C}_6\text{H}_{12})- m(\text{C}_6\text{D}_{6}) = (9.289710 \pm 0.000024)\times 10^{-3}\amu\,.
$$

From **(a)**, it follows that $m(\atom{2}{D}) = 2.014101789 \pm 0.000000021\amu$. The binding energy is then $$
    B = \left[m(\atom{1}{H}) + m(n)-m(\atom{2}{H})\right]c^2 = 2.22463\pm 0.0004 \MeV\,.
$$
One can also determine the binding energy by bringing together an unbound proton and neutron together to form $\atom{2}{H}$, and measuring the energy of the photon emitted (plus a recoil correction):
$$
    \atom{1}{H} + n \rightarrow \atom{2}{H} + \gamma\,.
$$
This reaction can be performed in reverse; determining the minimum photon energy required to produce deuterium (less the recoil energy).

Given that the average binding energy per nucleon [is about $8\MeV$](binding-energy.md#Binding-Energy), it follows that the deuteron is very weakly bound in comparison to typical nuclei.
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
The total angular momentum $I$ of the deuteron is given by the sum of the angular momenta of the nucleons, which add according to a set of [addition rules](../../quantum-mechanics/angular-momentum-addition.md). We can consider the total angular momentum $\hat{I}$ as 
$$
\vb{\hat{I}} = \vb{\hat{L}}_1 + \vb{\hat{S}}_1 + \vb{\hat{L}}_2 + \vb{\hat{S}}_2\,.
$$
It is conventional to consider the addition of the orbital angular momentum of the entire system and the individual spins:
$$
\tag{b}
\vb{\hat{I}} = \vb{\hat{L}} + \vb{\hat{S}}_1 + \vb{\hat{S}}_2\,,
$$
though one could also express $I$ in terms of the total orbital and spin operators
$$
\vb{\hat{I}} = \vb{\hat{L}} + \vb{\hat{S}}\,.
$$
<!-- TODO, can't we determine this from I = J2 + J2 = L1 + S1 + L2 + S2? -->
As $s=\frac{1}{2}$ particles, both the proton and neutron can have either $m_s=-\frac{1}{2}$ or $m_s=+\frac{1}{2}$, denoted as $\ket{-}$ and $\ket{+}$ respectively. Hence, in terms of *direct product states*, the total spin state must be one of
$$
\begin{matrix}
\ket{+}\ket{+}\\
\ket{-}\ket{+}\\
\ket{+}\ket{-}\\
\ket{-}\ket{-}\\
\end{matrix}
$$
From the addition rules, in the basis given by the eigenkets of the total operators $\vb{\hat{S}}_z$ and $\hat{S}$, the $z$ spin projection $m_s$ is given by $m_s=m_s^{(1)} + m_s^{(2)}$. Furthermore, the total spin $s$ is given by the equality $\abs{j_1-j_2}\leq j\leq j_1+j_2$, which for $s_i=\frac{1}{2}$ yields the following integer values $s=0,\,1$. It follows that the spin states of our system in the *total basis* are as follows:

For $m_s^{(1)}=m_s^{(2)}=\frac{1}{2}$, $m_s$ is maximised and thus equal to $s$, therefore $\ket{+}\ket{+}$ corresponds to $\ket{s=1,m_s=1}$ in this new basis. Given that $m_s=-s,\dots,\,+s$ it follows that this is a *triplet* state with $m_s=-1,\,\dots 0,\,1$. As we must have the same number of states in either basis, it follows that the remaining state is a *singlet* state $\ket{s=0,m_s=0}$

[^1]: Krane, p. 81.