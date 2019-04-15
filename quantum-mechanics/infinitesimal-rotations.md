Infinitesimal Rotations
=======================

<!-- Use vb rather than vec here as incorrect braket sizes ensue otherwise -->
Classical Mechanics
-------------------
Consider the orthogonal rotation matrices $R_{xyz}$ which represent a finite rotations about each axis
$$
R_z(\epsilon) = \begin{bmatrix}
\cos(\phi) & -\sin(\phi) & 0 \\
\sin(\phi) & \cos(\phi) & 0 \\
0 & 0 & 1
\end{bmatrix}\,,
$$
<!-- TODO taylor series -->
To find an infinitesimal form of $R_z$, let us take the [Taylor expansion](../maths/taylor-series.md) of $R_z(\epsilon)$ about $\epsilon=0$ to second order,
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
Rotation matrices in 3D belong to the SO(3) group, which stands for *special* (unit determinant) *unitary orthogonal 3D* group. The SO(3) group is _locally_ isomorphic (behaves locally in the same way) to the SU(2) group for a spin $\frac{1}{2}$ system, in that both characterise a *rotation*, but there is a *two-to-one* mapping from SO(3) to SU(2) i.e. $U(a,b)$ and $U(-a,-b)$ both map to a single $3\times3$ matrix in SO(3)[^1].

Infinitesimal Rotations in Quantum Mechanics
--------------------------------------------
$\gdef\D#1{\mathscr{D}(#1)}$
$\gdef\J#1{\hat{J}_{#1}})$
For Quantum Mechanics, the state key of a rotated system is _different_ to that of the unrotated system. Hence, for some rotation $R$, there is an associated rotation operator $\mathscr{D}(R)$, such that
$$
\ket{\alpha}_R = \D{R}\ket{\alpha}\,.
$$

The dimensionality of $\mathscr{D}(R)$ depends upon the dimensionality of the ket space upon which it operates. Classically, angular momentum generates rotations, just as linear momentum generates translations.
To find $\mathscr{D}(R)$, let us first consider a similar form as the [translation operator](infinitesimal-translations.md)
$$
\D{\vu{n},\dd\phi} = 1 - i\frac{\vb{\hat{J}}\cdot\vu{n}}{\hbar}\dd\phi\,,
$$
where $\vb{\hat{J}}$ is *defined such that* $\mathscr{D}$ has the above form.
As for finite translations, a finite rotation may be produced form a series of infinitesimal transformations, thus
$$
\D{\vu{n},\phi} = \exp\mleftright{(}{\frac{-i\vb{\hat{J}}\cdot\vu{n}}{\hbar}\phi}{)}\,.
$$
One might also postulate that $\D{R}$ has the same [group](../maths/group.md) properties as $R$.

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
Given that rotation operators *do not commute*, the group is therefore *non-Abelian*.

<!-- TODO p.218 simple examples of angular momentum addition

[^1]: https://pdfs.semanticscholar.org/60ef/f0e4956a3e4789bdd0395a87eb5ffc6d9b87.pdf