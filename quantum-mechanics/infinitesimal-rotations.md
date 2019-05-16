Infinitesimal Rotations
=======================

Classical Mechanics
-------------------

Consider the orthogonal rotation matrices $R_{xyz}$ which represent a finite rotations about each axis

$$
R_z(\phi) = \begin{bmatrix}
\cos(\phi) & -\sin(\phi) & 0 \\
\sin(\phi) & \cos(\phi) & 0 \\
0 & 0 & 1
\end{bmatrix}\,,
$$

<!-- TODO taylor series -->

To find an infinitesimal form of $R_z$, let us take the [Taylor expansion](../maths/taylor-series.md) of $R_z(\phi)$ about $\epsilon=0$ to second order,

$$
R_z(\epsilon) = \begin{bmatrix}
1-\frac{\epsilon^2}{2} & -\epsilon & 0 \\
\epsilon & 1-\frac{\epsilon^2}{2} & 0 \\
0 & 0 & 1
\end{bmatrix}\,,
$$

where $R_x$ and $R_y$ can be obtained by rolling along the diagonal according to cycling permutations of $x,y,z$. It should be noted that rotations about different axes _do_ commute when terms of $\mathcal{O}(\epsilon^2)$ or greater are ignored.

$$
R_x(\epsilon)R_y(\epsilon) = \begin{bmatrix}
1-\frac{\epsilon^2}{2} & 0 & \epsilon \\
\epsilon^2 & 1-\frac{\epsilon^2}{2} & -\epsilon\\
-\epsilon & \epsilon & 1-\epsilon^2
\end{bmatrix}\;\,
$$

$$
R_y(\epsilon)R_x(\epsilon) = \begin{bmatrix}
1-\frac{\epsilon^2}{2} & \epsilon^2 & \epsilon \\
0 & 1-\frac{\epsilon^2}{2} & -\epsilon\\
-\epsilon & \epsilon & 1-\epsilon^2
\end{bmatrix}\,.
$$

$$
R_x(\epsilon)R_y(\epsilon) - R_y(\epsilon)R_x(\epsilon) = \begin{bmatrix}
0 & -\epsilon^2 & 0\\
-\epsilon^2 & 0 & 0 \\
0 & 0 & 0\\
\end{bmatrix} = R_z(\epsilon^2)-I\,.
$$

Rotation matrices in 3D belong to the SO(3) group, which stands for _special_ (unit determinant) _unitary orthogonal 3D_ group. The SO(3) group is _locally_ isomorphic (behaves locally in the same way) to the SU(2) group for a spin $\frac{1}{2}$ system, in that both characterise a _rotation_, but there is a _two-to-one_ mapping from SO(3) to SU(2) i.e. $U(a,b)$ and $U(-a,-b)$ both map to a single $3\times3$ matrix in SO(3)[^1].

## Infinitesimal Rotations in Quantum Mechanics

$\gdef\D#1{\mathscr{D}(#1)}$
$\gdef\J#1{\hat{J}_{#1}}$
For Quantum Mechanics, the state key of a rotated system is _different_ to that of the unrotated system. Hence, for some rotation $R$, there is an associated rotation operator $\mathscr{D}(R)$, such that

$$
\ket{\alpha}_R = \D{R}\ket{\alpha}\,.
$$

The dimensionality of $\mathscr{D}(R)$ depends upon the dimensionality of the ket space upon which it operates. Classically, angular momentum generates rotations, just as linear momentum generates translations.
To find $\mathscr{D}(R)$, let us first consider a similar form as the [translation operator](infinitesimal-translations.md)

$$
\D{\vu{n},\dd\phi} = 1 - i\frac{\vb{\hat{J}}\cdot\vu{n}}{\hbar}\dd\phi\,,
$$

where $\vb{\hat{J}}$ is _defined such that_ $\mathscr{D}$ has the above form, i.e. $\hat{J}_k$ generates a rotation about $\vu{k}$ .
As for finite translations, a finite rotation may be produced form a series of infinitesimal transformations, thus

$$
\D{\vu{n},\phi} = \exp\mleftright{(}{\frac{-i\vb{\hat{J}}\cdot\vu{n}}{\hbar}\phi}{)}\,.
$$

One might also postulate that $\D{R}$ has the same [group](../maths/group.md) properties as $R$. Evidently, $\mathscr{D}$ must be unitary in order to preserve the inner product.

The fundamental commutation relations for rotation operations may be written for $\mathscr{D}$

$$
\begin{aligned}
\comm{\D{\vu{x},\epsilon}}{\D{\vu{y},\epsilon}} &= \comm{
    1-\frac{i\J{x}\epsilon}{\hbar}-\frac{\J{x}^2\epsilon^2}{2\hbar^2}+\mathcal{O}\mleftright{[}{\epsilon^3}{]}
}{
    1-\frac{i\J{y}\epsilon}{\hbar}-\frac{\J{y}^2\epsilon^2}{2\hbar^2}+\mathcal{O}\mleftright{[}{\epsilon^3}{]}
}\\
&= 1-\frac{i\J{z}\epsilon^2}{\hbar}-1\,.
\end{aligned}
$$

Equating terms of order $\epsilon^2$ on both sides we obtain

$$
\comm{\J{x}}{\J{y}} = i\hbar \J{z}\,,
$$

which is generalised to all axes as

$$
\comm{\J{i}}{\J{j}} = i\hbar \varepsilon_{ijk}\J{k}\,.
$$

Given that rotation operators _do not commute_, the group is therefore _non-Abelian_.

The Rotation Operator in the Angular-Momentum Eigenbasis
--------------------------------------------------------
<!-- TODO link this to tensors notes -->
Consider the general state ket $\alpha$ with a known $j$. Expressed in the eigenbasis of $\hat{J}_z$, we have
$$
\ket{\alpha} = \sum_m\alpha_m\ket{jm}\,.
$$
The rotated state $\ket{\alpha'}$ is given by 
$$
\begin{aligned}
\ket{\alpha'}
&= \mathscr{D}{R}\ket{\alpha}\\
&= \sum_m\alpha_m\mathscr{D}(R)\ket{jm}\,.
\end{aligned}
$$
Inserting the identity, we have
$$
\begin{aligned}
\ket{\alpha'} 
&= \sum_{nm}\alpha_m\ketbra{jn}{jn}\mathscr{D}(R)\ket{jm}\\
&= \sum_{nm}\alpha_m\mathscr{D}^{(j)}_{nm}(R)\ket{jn}\,.
\end{aligned}
$$
It follows that under $\mathscr{D}$, the components $\alpha$ transform as 
$$
\alpha_n\rightarrow \sum_m \alpha_m\mathscr{D}^{(j)}_{nm}(R)\,.
$$
When acting on the base ket, we find
$$
\begin{aligned}
\mathscr{D}(R)\ket{jm} 
&= \sum_n\ketbra{jn}{jn}\mathscr{D}(R)\ket{jm}\\
&= \sum_n\mathscr{D}^{(j)}_{nm}(R)\ket{jn}\,\,
\end{aligned}
$$
hence the base kets transform as 
$$
\ket{jm} \rightarrow \sum_n\mathscr{D}^{(j)}_{nm}(R)\ket{jn} 
$$
$$
\begin{aligned}
\ket{\overline{\phi}} &= \mathscr{D}(R)\ket{\phi}\\
\ket{\overline{\psi}} &= \mathscr{D}(R)\ket{\psi}
\end{aligned}
$$

Now, an operator transforms between two bases under $\hat{U}$ as
$$
\def\U{\hat{U}}
\def\O{\hat{O}}
\begin{aligned}
\ket{\psi} &= \O\ket{\phi}\\
\ket{\psi'} &=  \U \O \ket{\phi}\\
&= \U\O\U^\dagger\U\ket{\phi}\\
&= \U\O\U^\dagger\ket{\phi'}\,,
\end{aligned}
$$
i.e. $$\hat{O}\rightarrow\hat{U}\hat{O}\hat{U}^\dagger\,.$$

Vector & Scalar Operators
-------------------------
A *vector operator* is defined as a set of operators which transform like classical vector components under rotation, i.e. $$\hat{V}'_i = '\hat{U}\hat{V}_i\hat{U}^\dagger=\sum R_{ij}\hat{V}_j\,.$$
A *scalar operator* is defined as an operator which is invariant under rotations, i.e. $$\hat{S} = \hat{U}\hat{S}\hat{U}^\dagger\,.$$
It is interesting to derive the commutation relations between vector operators and angular momenta. Consider the infinitesimal rotation matrix R_z
$$
R_z = \begin{pmatrix}1 & -\epsilon & 0 \\ \epsilon & 1 & 0 \\ 0 & 0 & 1\end{pmatrix}\,.
$$
The rotation operator associated with $R_z$ is 
$$
\mathscr{D}(R_z) = 1 - i\frac{\epsilon{\J}_z}{\hbar}\,.
$$
Hence, a vector operator component $\hat{V}_i$ in the rotated basis is given by
$$
\begin{aligned}
\mathscr{D}(R)\hat{V}_i\mathscr{D}(R)^\dagger 
&= \left(1-i\epsilon\frac{{\J}_z}{\hbar}\right)\hat{V}_i\left(1+i\epsilon\frac{{\J}_z}{\hbar}\right)\\
&= \hat{V}_i +\frac{i\epsilon}{\hbar}\left(\hat{V}_i{\J}_z-{\J}_z\hat{V}_i\right)\\
&= \hat{V}_i + \frac{i\epsilon}{\hbar}\comm{\hat{V}_i}{{\J}_z}\,.
\end{aligned}
$$
For the given matrix $R$ it follows that the transformed operator $\hat{V}'_1$ is
$$
\begin{aligned}
\mathscr{D}(R)\hat{V}_i\mathscr{D}(R)^\dagger =\hat{V}_1 -\epsilon\hat{V}_2\,,
\end{aligned}
$$
which gives
$$
\comm{\hat{V}_x}{{\J}_z} = i\hbar\hat{V}_y\,.
$$
It can easily be shown that
$$
\begin{aligned}
\comm{\hat{V}_y}{{\J}_z} &= -i\hbar\hat{V}_x\\
\comm{\hat{V}_z}{{\J}_z} &= 0\,,
\end{aligned}
$$
hence most generally we have
$$
\comm{\hat{V}_i}{{\J}_k} = -i\hbar\epsilon_{ijk}\hat{V}_k
$$
<!-- TODO
permute these to introduce levi civita and rectify ordering difference to http://galileo.phys.virginia.edu/classes/752.mf1i.spring03/TensorOperators.htm -->

<!-- TODO p.218 simple examples of angular momentum addition -->

[^1]: https://pdfs.semanticscholar.org/60ef/f0e4956a3e4789bdd0395a87eb5ffc6d9b87.pdf
