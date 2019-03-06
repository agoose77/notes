Radiation Interactions
======================
There are several major kinds of radiation which interact with matter, represented in the table below.

|             Charged Particulate Radiations            	|                  Uncharged Radiations                 	|
|:-----------------------------------------------------:	|:-----------------------------------------------------:	|
| Heavy charged particles $\sim10^{-5}\operatorname{m}$ 	|         Neutrons $\sim10^{-1}\operatorname{m}$        	|
| Fast electrons $\sim10^{-3}\operatorname{m}$          	| X-rays \& $\gamma$ rays $\sim10^{-1}\operatorname{m}$ 	|

As can be seen from the table, charged radiation has a typically shorter interaction distance than that of the uncharged variety. Charged radiation interacts _continuously_ with the medium through the Coulomb force, whereas uncharged radiation must first undergo a series of discrete interactions such as collisions.

Heavy Charged Particles
-----------------------
Heavy charged particles such as the $\alpha$ interact primarily through the coulomb force between the particles and orbital electrons within the absorber atoms. Direct interactions between the particles and nuclei _are possible_, though quite unlikely, and are usually insignificant in their effect upon the detector response.

Through the Coulomb force, the passage of a charged particle within an absorbing medium will apply an _impulse_ to the surrounding electrons. Depending upon the proximity of the encounter, the impulse may be sufficient to raise an electron to a higher energy level within the atom (_excitation_), or to remove it from the atom completely (_ionisation_). <!-- TODO: If not excited, how much E is transferred, and how is it dissipated? -->
When treated as an elastic collision, the [maximum energy transfer](../mechanics/2D-collisions.md#Energy-Transfer) from a charged particle of mass $m$ with kinetic energy $E$ to a static electron of mass $m_0$ is $\frac{4Em_0}{m}$. This value is so small that the primary particle must lose its energy through numerous repeated interactions during its passage through a material. 

For each interaction, the [deflection angle](../mechanics/2D-collisions.md#Deflection-Angle) is quite small (as $m \gg m_0$), and interactions occur in all directions simultaneously, hence _the tracks through the material tend to be quite straight_. Hence, charged particles are characterised by a definite _range_ in a given absorber material, which defines the distance beyond which no particles will penetrate.
<!-- TODO: No particles is invalid (?), more like, likelihood very small -->

The product of charged particle interactions will be excited atoms, or _ion pairs_. Each pair is composed of a free electron, and the corresponding positive ion of an absorber atom from which an electron has been removed. These pairs have a natural tendency to recombine to form neutral atoms, but in some detectors this may be suppressed such that the ion pairs are used as the basis of the detector response. In particularly close encounters, an electron may experience a large impulse such that, once unbound from its parent atom, it may have sufficient kinetic energy to create further ions. These _energetic electrons_ are called _delta rays_. Typically, the _majority_ of the energy of the charged particle is transferred via delta rays. _The range of these electrons is always small in comparison to the range of the incident charged particle_, so the ionisation remains close to the primary track.