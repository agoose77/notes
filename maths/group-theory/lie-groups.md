Lie Groups
==========

A continuous group is a group $G$ with an infinite number of elements $g \in G$ which depend continuously upon a set of parameters
$$
g = g(\alpha)\,,\; \alpha = \set{\alpha_i:i=1 \to N}\,.
$$
The *dimension* $\dim G = N$ of the group counts the number of continuous parameters.

A Lie group is a continuous group which admits an analytic structure in the parameters $\set{\alpha}$. One might alternatively say that a Lie group is a group which is also a differentiable manifold.[^wien.lie-groups]
<!-- TODO explain analytic structure or differentiable manifold 
<!-- TODO examples -->
<!-- TODO: [^wien.lie-groups] - 
$V$ is the space of 2x2 complex hermitian matrices with tr=0
$V$ can be parameterised by $x \in R^n$ with a basis of the Pauli matrices
With an inner product as $\innerproduct{x}{y} = \frac{1}{t}\trace{x\cdot y}$, the basis is found to be orthonormal
Now for some U in SU2, we can show that $UxU^{-1}$ is in $V$ for $x \in V$, so for the group SU2 we can define the action $\phi: SU(2)\times V \rightarrow V$, $\phi_U = UxU^{-1}$. Then if we take the trace of elements in V acted on by SU(2), we find it is equivalent to the original trace, so $\phi_U$ is an orthogonal transformation (length preserving), a homomorphism, and continiuous. It follows from orthogonality that $\phi$ (which maps an element from $U$ to an operation on $V$) is in $O(3)$, where 3 comes from the fact that $\dim(V)$ is 3.
From https://en.wikipedia.org/wiki/Orthogonal_group O(3) in real space are matrices with det = +- 1. SO(3) is the subgroup with det = +1
As SU(2) is connected and map $\phi$ is continuous, we preserve det|su(2)| = +1 and hence $\phi_U$ maps into SO(3).
  - questions: * are matrix representations of groups actually "representations" mapped by a homeomorphism. I.e. are members of GL(n) like O(3) actually matrices or is this some funky representation stuff
               * why is the determinant preserved by connected group and continuous map
                    TODO maybe see this https://link.springer.com/content/pdf/bbm%3A978-1-4757-2742-5%2F1.pdf
                * NV connected: [^symmetry-qm]
Thus $\phi$ is a Lie group homomorphism of SU(2) into SO(3) but NOT an isomorphism
-->

<!--
NOTE: [^nadir.tensors] clarifies that SU(2) is the three-sphere:
then $|\alpha|^{2}+|\beta|^{2}=1$ becomes
$$
u^{2}+v^{2}+x^{2}+y^{2}=1 % Three sphere with 4 coords
$$

Example 4.22. S U.2/ and SO.3/ - SU(3) vs SO(3)

SO(2) with real coordinates is clear just unit circle.
-->
<!-- TODO: SO3 vs O3 https://www.physics.rutgers.edu/grad/618/lects/infinite.pdf -->

<div style="padding:15px;margin-bottom:20px;border:1px solid transparent;border-radius:4px;color:#31708f;background-color:#d9edf7
;border-color:#bce8f1;">
    
### General Linear Groups
<!-- Here the semicolon distinguishes variables but is semantically identical to a comma -->
The *general linear group* over the reals $\operatorname{GL}(n;\mathbb{R})$ is the [group](../group.md) of all $n\times n$ invertible matrices with real entries. There is similarly the linear operator $\operatorname{GL}(n;\mathbb{C})$ defined over the complex numbers. 
    
The group property under the binary operation of matrix multiplication $(\cdot\times\cdot)$ follows from the [group axioms](../group.md#Group-Axioms):
* Matrix multiplication is associative (*associativity*)
* The product $(\mathbf{A}\times \mathbf{B})$ of two invertible matrices $\mathbf{A},\mathbf{B}$ is itself invertible (*closure*)
* There exists an identity matrix $\mathbf{\mathbb{I}}$ (*identity element*)
* There exists an inverse (by definition) for all invertible matrices (*inverse element*)
</div>

<div style="padding:15px;margin-bottom:20px;border:1px solid transparent;border-radius:4px;color:#31708f;background-color:#d9edf7
;border-color:#bce8f1;">

### Convergence
A matrix series $\mathbf{A_m}$ is said to converge to some matrix $\mathbf{A}$ if each element $kl$ of $\mathbf{A_m}$ converges to the corresponding element of $\mathbf{A}$, i.e. $(A_m)_{kl}\rightarrow A_{kl} \forall\,kl$.
</div>
    
<div style="padding:15px;margin-bottom:20px;border:1px solid transparent;border-radius:4px;color:#31708f;background-color:#d9edf7
;border-color:#bce8f1;">
    
### Matrix Lie Group
<!-- Here the semicolon distinguishes variables but is semantically identical to a comma -->
A matrix Lie group is any subgroup G of $\operatorname{GL}(n;\mathbb{C})$ which satisfies the following:
    
> If $A_m$ is a sequence of matrices in $G$ and $A_m$ converges to some matrix $A$ then either $A\in G$ or $A$ is not invertible.[^hall]
    
In simpler it is a Lie group whose elements are matrices.[^lloyd]
</div>


<!-- Note interesting isomorphism between SO(2) ≈ SU(1).[^lloyd]`` -->

* The geometric link between a Lie group and its Lie algebra is the fact that the Lie algebra can be viewed as the tangent space to the Lie group at the identity.[^geom]
* There is a map from the tangent space to the Lie group, called the exponential map:
  $$\exp\colon \mathfrak{so}(n) \rightarrow \mathbf{SO}(n)$$
* Hence, as a tangent space the Lie algebra is a *linearisation* of the lie group
  See work on manifolds
$$\mathfrak{so}(n, \mathbb{R})$$

[^geom]: https://www.cis.upenn.edu/~cis610/geombchap14.pdf
[^lloyd]: https://www.whitman.edu/documents/Academics/Mathematics/2015/Final%20Project%20-%20Lloyd.pdf
[^hall]: Brian С Hall Lie Groups, Lie Algebras, and Representations An Elementary Introduction
<!-- TODO reread below links -->
[^symmetry-qm]: https://www2.ph.ed.ac.uk/~rzwicky2/SoQM/romanSoQM_2015.pdf
[^surrey.james]: http://personal.maths.surrey.ac.uk/st/A.Torrielli/files/JamesNotes.pdf 
[^wien.lie-groups]: https://homepage.univie.ac.at/harold.steinacker/LieVl-2015.pdf
[^ua.lie]: http://gravitation.web.ua.pt/sites/default/files/migrated2016/LieGroups.pdf
[^nadir.tensors]: An Introduction to Tensors and Group Theory for Physicists, Nadir Jeevanjee.