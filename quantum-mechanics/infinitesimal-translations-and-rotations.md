Infinitesimal Translations and Rotations
========================================
Infinitesimal Rotations in Cartesian Space
------------------------------------------
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
\left\vert{\alpha}\right\rangle_R = \mathscr{D}(R)\left\vert{\alpha}\right\rangle\,.
$$
<!--
\left\langle {x} \right\vert .
\left\vert {x } \right\rangle
-->

The dimensionality of $\mathscr{D}(R)$ depends upon the dimensionality of the ket space upon which it operates. Classically, angular momentum generates rotations, just as linear momentum generates translations.
To find $\mathscr{D}(R)$, let us first consider _translations_.

Let $\mathscr{T}(\mathrm{d}\boldsymbol{x'})$ be the operator such that
$$
\mathscr{T}(\mathrm{d}\boldsymbol{x'})\left\vert{\boldsymbol{x'}}\right\rangle = \left\vert{\boldsymbol{x'}+\mathrm{d}\boldsymbol{x'}}\right\rangle
$$

<!--
/\\ket\[([^\]]*)\]/ -> \\left\\vert\{$1\}\\right\\rangle
/\\bra\[([^\]]*)\]/ -> \\left\\langle\{$1\}\\right\\vert

# Bra
/\\left\\vert\{(.*?)\}\\right\\rangle/
# Ket
/\\left\\langle\{(.*?)\}\\right\\vert/
-->

Consider some state $\left\vert{\alpha}\right\rangle$. Under $\mathscr{T}(\mathrm{d}\boldsymbol{x'})$, it behaves as follows
$$
\begin{aligned}
\mathscr{T}(\mathrm{d}\boldsymbol{x'})\left\vert{\alpha}\right\rangle &= \mathscr{T}(\mathrm{d}\boldsymbol{x'})\boldsymbol{1}\left\vert{\alpha}\right\rangle \\
&= \mathscr{T}(\mathrm{d}\boldsymbol{x'})\int\left\vert{\boldsymbol{x}'}\right\rangle\left\langle{\boldsymbol{x}'}\right\vert\,\mathrm{d}^3\boldsymbol{x'}\left\vert{\alpha}\right\rangle \\
&= \int\left\vert{\boldsymbol{x}'+\mathrm{d}\boldsymbol{x'}}\right\rangle\left\langle{\boldsymbol{x}'}\right\vert\,\mathrm{d}^3\boldsymbol{x'}\left\vert{\alpha}\right\rangle \,,
\end{aligned}
$$
which is equivalent to 
$$
\mathscr{T}(\mathrm{d}\boldsymbol{x'})\left\vert{\alpha}\right\rangle = \int\left\vert{\boldsymbol{x}'}\right\rangle\left\langle{\boldsymbol{x}'-\mathrm{d}\boldsymbol{x'}}\right\vert\,\mathrm{d}^3\boldsymbol{x'}\left\vert{\alpha}\right\rangle \,,
$$
as the integral is over _all space_.

What are the properties of $\mathscr{T}$?
If $\left\vert{\alpha}\right\rangle$ is normalised then $\mathscr{T}(\mathrm{d}\boldsymbol{x'})\left\vert{\alpha}\right\rangle$ ought to remain so, 
$$
\left\langle{\alpha}\right\vert\mathscr{T}(\mathrm{d}\boldsymbol{x'})^\dagger\mathscr{T}(\mathrm{d}\boldsymbol{x'})\left\vert{\alpha}\right\rangle = 1\,,
$$

hence $\mathscr{T}^\dagger\mathscr{T} = 1$, i.e. $\mathscr{T}$ must be [unitary](../maths/linear-algebra/square-matrices.md#Unitary%20%5BNormal%5D).