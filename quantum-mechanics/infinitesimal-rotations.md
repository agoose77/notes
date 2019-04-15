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

Infinitesimal Rotations in Quantum Mechanics
--------------------------------------------
For Quantum Mechanics, the state key of a rotated system is _different_ to that of the unrotated system. Hence, for some rotation $R$, there is an associated rotation operator $\mathscr{D}(R)$, such that
$$
\ket{\alpha}_R = \mathscr{D}(R)\ket{\alpha}\,.
$$

The dimensionality of $\mathscr{D}(R)$ depends upon the dimensionality of the ket space upon which it operates. Classically, angular momentum generates rotations, just as linear momentum generates translations.
To find $\mathscr{D}(R)$, let us first consider a similar form as the [translation operator](infinitesimal-translations.md)
$$
\mathscr{D}(\vu{n},\dd\phi) = 1 - i\frac{\vb{\hat{J}}\cdot\vu{n}}{\hbar}\dd\phi\,.
$$
As for finite translations, a finite rotation may be produced form a series of infinitesimal transformations, thus
$$
\mathscr{D}(\vu{n},\phi) = \exp\mleftright{(}{\frac{-i\vb{\hat{J}}\cdot\vu{n}}{\hbar}\phi}{)}\,.
$$