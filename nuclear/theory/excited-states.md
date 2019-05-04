Excited States
==============

Excited states are produced by adding _vibrational_ or _rotational_ energy to the nucleus. This energy may be sufficient to break a nucleon pair, thereby adding two valence neutrons. They are measured relative to the reference *ground state*.

Density of States
-----------------
<!-- TODO link fermi-dirac -->
Nuclei are composed of nucleons, which obey Fermi-Dirac statics (i.e. they are fermions). As such, any two identicle nucleons cannot obey the same (single-particle) state. Ignoring particle interactions, it follows that the state of the nucleus may be constructed from a set of distinct single-particle states. The lowest energy (ground) may be constructed by poopulating these states in order of ascending energy. From this process a *surface* between the highest energy populated state, and the first (lowest) unpopulated state, known as the *Fermi level*. Excitations of the nucleus will thus promote nucleons into single particle states *above* the Fermi level. At low excitation energies $E$, only those particles in states near the surface (for which the "work function" $\Delta E$ satisfies $\Delta E \leq E$) may populate these excited states. As $E$ increases, it follows that a greater number of particles can be promoted, and the number of *independent* ways in which these operations may be performed increases. This gives rise to the *Fermi gas model* of the density of states
$$
\tag{1}
\rho_A(E)=\frac{1}{12a^\frac{1}{4}E^\frac{5}{4}}e^{2\sqrt{aE}}\,.
$$
In order to construct this model, it was assumed that particle interactions were neglible. Though this is not the case, the model can be used to inspect the general properties of the nucleus. Interactions between particles act in part to shift the energy of the ground state, which can be modelled through a linear translation 
$$
\tag{2}
\rho_A(E)=\frac{1}{12a^\frac{1}{4}(E-\Delta)^\frac{5}{4}}e^{2\sqrt{a(E-\Delta)}}\,.
$$
**(2)** is called the *backshifted* Ferm gas model.

<!-- TODO flesh this out -->
