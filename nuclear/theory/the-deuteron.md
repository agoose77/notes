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
$\gdef\S{\hat{S}}$
The total angular momentum $I$ of the deuteron is given by the sum of the angular momenta of the nucleons, which add according to a set of [addition rules](../../quantum-mechanics/angular-momentum-addition.md). We can consider the total angular momentum $\hat{I}$ as 
$$
\vb{\hat{I}} = \vb{\hat{L}}_1 + \vb{\S}_1 + \vb{\hat{L}}_2 + \vb{\S}_2\,.
$$
It is conventional to consider the addition of the orbital angular momentum of the entire system and the individual spins:
$$
\tag{b}
\vb{\hat{I}} = \vb{\hat{L}} + \vb{\S}_1 + \vb{\S}_2\,,
$$
though one could also express $I$ in terms of the total orbital and spin operators
$$
\vb{\hat{I}} = \vb{\hat{L}} + \vb{\S}\,.
$$

From [addition of the two spins](../../quantum-mechanics/two-particle-spin-half-states.md), the total spin $S$ has a singlet state $\ket{s=0;m_s=0}$ and a triplet state $\ket{s=1;m_s=\pm 1,0}$
In nature, the deuteron is observed to have $I=1$. We may determine which states couple to produce $I=1$, given that $S\in\set{0,\,1}$ and $L\geq 0$:
| $L$ 	| $S$ 	| $\set{I}$         	|
|:---:	|:---:	|-------------------	|
|  0  	|  0  	| $\set{0}$         	|
|  0  	|  1  	| $\set{1}$         	|
|  1  	|  0  	| $\set{1}$         	|
| 1   	| 1   	| $\set{0,\,1,\,2}$ 	|
| 2   	| 0   	| $\set{2}$         	|
| 2   	| 1   	| $\set{1,\,2}$     	|
Evidently, there are four ways to couple $L$ and $S$ to produce $I=1$. 

<!-- 
TODO
deuteron has +ve parity (assume of w.f., define this). Parity of orbital wf comes from (-1)^l. Need to understand parity vs exchange: https://www.physicsforums.com/threads/particle-exchange-and-parity.493128/post-3265145, https://physics.stackexchange.com/a/149015
Maybe http://www.damtp.cam.ac.uk/user/tong/aqm/aqmfive.pdf
Look at isospin - what governs composite system of fermionss?
-->

[^1]: Krane, p. 81.