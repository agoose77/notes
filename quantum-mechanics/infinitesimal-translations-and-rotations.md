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
\ket{\alpha}_R = \mathscr{D}(R)\ket{\alpha}\,.
$$

The dimensionality of $\mathscr{D}(R)$ depends upon the dimensionality of the ket space upon which it operates. Classically, angular momentum generates rotations, just as linear momentum generates translations.
To find $\mathscr{D}(R)$, let us first consider _translations_.

Infinitesimal Translations in Quantum Mechanics
-----------------------------------------------
<!-- Define custom macros -->
$\gdef\xp{\em{x'}}$ 
$\gdef\T#1{\mathscr{T}(#1)}$
$\gdef\X{\hat{\em{X}}}$

Let $\T{\dd\xp}$ be the operator such that
$$
\T{\dd\xp}\ket{\xp} = \ket{\xp+\dd\xp}\,.
$$
N.B. that $\ket{\em{x}} = \ket{x}\otimes\ket{y}\otimes\ket{y}$, i.e. there is a unique position space for each coordinate.

Consider some state $\ket{\alpha}$. Under $\T{\dd\xp}$, it behaves as follows
$$
\begin{aligned}
\T{\dd\xp}\ket{\alpha} &= \T{\dd\xp}\em{1}\ket{\alpha} \\
&= \T{\dd\xp}\int\ket{\xp}\bra{\xp}\,\mathrm{d}^3\xp\ket{\alpha} \\
&= \int\ket{\xp+\dd\xp}\bra{\xp}\,\mathrm{d}^3\xp\ket{\alpha} \,,
\end{aligned}
$$
which is equivalent to 
$$
\T{\dd\xp}\ket{\alpha} = \int\ket{\xp}\bra{\xp-\dd\xp}\dd^3\xp\ket{\alpha} \,,
$$
as the integral is over _all space_.

What are the properties of $\mathscr{T}$?
1. If $\ket{\alpha}$ is normalised then $\T{\dd\xp}\ket{\alpha}$ ought to remain so, 
$$
\bra{\alpha}\T{\dd\xp}^\dagger\T{\dd\xp}\ket{\alpha} = 1\,,
$$
hence $\mathscr{T}^\dagger\mathscr{T} = 1$, i.e. $\mathscr{T}$ must be [unitary](../maths/linear-algebra/square-matrices.md#Unitary%20%5BNormal%5D).
1. $\T{\dd\xp}\T{\em{x''}}=\T{\dd\xp+\dd\em{x''}}$
1. $\T{-\dd\xp}\T{\dd\xp}=\em{1}$.
1. $\lim\limits_{\dd\xp\rightarrow 0}\T{\dd\xp}=\em{1}$

Let us consider an operator of the form $\T{\dd\xp}=1-i\em{k}\cdot\dd\xp$. Ignoring all $\mathcal{O}(\dd\xp^2)$ terms, it can be shown through Taylor expansion that all of the above conditions are satisfied.

With the $\X$ operator, we derive the following behaviour
$$
\begin{aligned}
\X\T{\dd\xp}\ket{\xp} &= \X\ket{\xp+\dd\xp}\\
                      &= (\xp + \dd\xp)\ket{\xp+\dd\xp}\\
\T{\dd\xp}\X\ket{\xp} &= \xp\T{\dd\xp}\ket{\xp}\\
                      &= \xp\ket{\xp+\dd\xp}\,,
\end{aligned}
$$

hence
$$
\begin{aligned}
\comm{\X}{\T{\dd\xp}}\ket{\xp} &= \dd\xp\ket{\xp+\dd\xp}\\
                               &= \dd{\xp}\T{\dd\xp}\ket{\xp}\,.
\end{aligned}
$$

<!-- TODO check this derivation in Sakurai -->
Using the above definition of $\mathscr{T}$:
$$
\begin{aligned}
\X&(1-\em{k}i\cdot\dd\xp) - (1-i\em{k}\cdot\dd\xp)\X\\
&= -i(\X\em{k}\cdot\dd\xp-\em{k}\cdot\dd\xp\X)\\
&= (1-i\em{k}\cdot\dd\xp)\dd\xp\\
&\approx \dd\xp
\end{aligned}
$$