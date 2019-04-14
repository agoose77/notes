Infinitesimal Translations and Rotations
========================================
<!-- Use vb rather than vec here as incorrect braket sizes ensue otherwise -->
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
$\gdef\xp{\vb{x'}}$ 
$\gdef\T#1{\mathscr{T}(#1)}$
$\gdef\X{\hat{\vb{X}}}$

Let $\T{\dd\xp}$ be the operator such that
$$
\T{\dd\xp}\ket{\xp} = \ket{\xp+\dd\xp}\,.
$$
N.B. that $\ket{\vec{x}} = \ket{x}\otimes\ket{y}\otimes\ket{y}$, i.e. there is a unique position space for each coordinate.

Consider some state $\ket{\alpha}$. Under $\T{\dd\xp}$, it behaves as follows
$$
\begin{aligned}
\T{\dd\xp}\ket{\alpha} &= \T{\dd\xp}1\ket{\alpha} \\
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
hence $\mathscr{T}^\dagger\mathscr{T} = 1$ (where $1$ is the identity operator), i.e. $\mathscr{T}$ must be [unitary](../maths/linear-algebra/square-matrices.md#Unitary%20%5BNormal%5D).
1. $\T{\dd\xp}\T{\vb{x''}}=\T{\dd\xp+\dd\vb{x''}}$
1. $\T{-\dd\xp}\T{\dd\xp}=1$
1. $\lim\limits_{\dd\xp\rightarrow 0}\T{\dd\xp}=1$

Let us consider an operator of the form $\T{\dd\xp}=1-i\vb{K}\cdot\dd\xp$. Ignoring all $\mathcal{O}(\dd\xp^2)$ terms, it can be shown through Taylor expansion that all of the above conditions are satisfied.

With the $\X$ operator, we derive the following behaviour
$$
\begin{aligned}
\X\T{\dd\xp}\ket{\xp} &= \X\ket{\xp+\dd\xp}\\
                      &= (\xp + \dd\xp)\ket{\xp+\dd\xp}\\
\T{\dd\xp}\X\ket{\xp} &= \xp\T{\dd\xp}\ket{\xp}\\
                      &= \xp\ket{\xp+\dd\xp}\,,
\end{aligned}
$$

hence we have the operator identity
$$
\begin{aligned}
\comm{\X}{\T{\dd\xp}}\ket{\xp} &= \dd\xp\ket{\xp+\dd\xp}\\
                               &\approx \dd{\xp}\ket{\xp}\,.
\end{aligned}
$$

<!-- TODO check this derivation in Sakurai -->
Using the above definition of $\mathscr{T}$ to first order this may be written as
$$
\X(1-\vb{K}i\cdot\dd\xp) - (1-i\vb{K}\cdot\dd\xp)\X = \dd\xp\,,
$$
where implicitly $\dd\xp$ is multiplied by the identity operator. In terms of each coordinate, it then follows that
$$
-i\comm{\hat{x_i}}{\vb{K}\cdot\dd\xp} = \dd x'_i\,.
$$

Let $\dd x'_j=\epsilon$, $\dd x'_{p\neq j}=0$, then
$$
\begin{aligned}
-i\comm{x_i}{K_j\epsilon} &= \dd x'_i \\
                          &= \delta_{ij}\epsilon\,,
\end{aligned}
$$
which gives
$$
\tag{a}
\comm{x_i}{K_j} = i\delta_{ij}\,.
$$

These results indicate that $K$ is a _generator_ of translation, in a manner analagous to _momentum_ in classical mechanics. However, as a coefficient of a quantum state, $\vb{K}\cdot\dd\xp$ must be dimensionless, and thus there must be a _constant of action_ to render $\vb{K}$ dimensionless. It transpires that this constant is simple $\hbar$, and thus
$$
\T{\dd\xp} = 1-\frac{i\vb{p}\cdot\dd\xp}{\hbar}\,.
$$
The commutation relation **(a)** now becomes 
$$
\comm{x_i}{p_j} = i\hbar\delta_{ij}\,.
$$

<!-- TODO should we introduce Heisenberg uncertainty relation here? 
Let us then consider a translation operator of finite translaion $\T{\Delta\xp}$, which can be produced by compounding a series of inifinitesimal translations
$$
\begin{aligned}
\T{\Delta\xp} &= \lim_{N\rightarrow\infty}\left(1-\frac{i\vb{p}\cdot\Delta\xp}{N\hbar}\right)^N\\
              &= \exp\left(-\frac{i\vb{p}\cdot\Delta\xp}{\hbar}\right)\,.
\end{aligned}
$$
<!-- TODO matrix exponential -#->
Here, $\T{\Delta\xp}$ is a [matrix exponential](../maths/matrix-exponential.md) operator.
-->

<!-- TODO should we introduce Heisenberg uncertainty relation here? -->
Let us then consider a translation operator of finite translaion $\T{\Delta x'\vu{x}}$, where $\vu{x}$ is the unit $x$ vector, which can be produced by compounding a series of inifinitesimal translations
$$
\begin{aligned}
\T{\Delta\xp} &= \lim_{N\rightarrow\infty}\left(1-\frac{ip_x\Delta x'}{N\hbar}\right)^N\\
              &= \exp\left(\frac{-ip_x\Delta x'}{\hbar}\right)\,.
\end{aligned}
$$
<!-- TODO matrix exponential -->
Here, $ \exp\left(\frac{-ip_x\Delta x'}{\hbar}\right)$ is a [matrix exponential](../maths/matrix-exponential.md). A fundamental property of translations is that translations in different directions commute, and thus form an [Abelian group](../maths/group.md#Abelian-Groups).
<!-- TODO check all URLS dont 404 -->Therefore, we must have 
$$
\begin{aligned}
\T{\Delta x'\vu{x}}\T{\Delta y'\vu{y}} &= \T{\Delta x'\vu{x} + \Delta y'\vu{y}}\\
\T{\Delta y'\vu{y}}\T{\Delta x'\vu{x}} &= \T{\Delta y'\vu{y} + \Delta x'\vu{x}}\,.
\end{aligned}
$$
To second order, this commutation relation expands as follows 
$$
\begin{aligned}
\comm{\T{\Delta x'\vu{x}}}{\T{\Delta y'\vu{y}}} &= \comm{
    1-\frac{ip_x\Delta x'}{\hbar}-\frac{p_x^2(\Delta x')^2}{2\hbar^2}+\mathcal{O}\mleftright{[}{(\Delta x')^3}{]}
}{
    1-\frac{ip_y\Delta y'}{\hbar}-\frac{p_y^2(\Delta y')^2}{2\hbar^2}+\mathcal{O}\mleftright{[}{(\Delta y')^3}{]}
}\\
&= -\frac{p_x\Delta x'}{\hbar}\frac{p_y\Delta y'}{\hbar} + \frac{p_y\Delta y'}{\hbar}\frac{p_x\Delta x'}{\hbar}\\
&= -\frac{\Delta x'\Delta y'}{\hbar^2}\comm{p_x}{p_y}\,.
\end{aligned}
$$
In order for translation operators to commute, a new commutation relation is thus introduced
$$
\tag{b}
\comm{p_x}{p_y} = 0\,.
$$

### Canonical Commutation Laws
We have now established the _canonical commutation laws_:
<!-- N.B. [xi,xj] follows from the fact that they are different position spaces. This also follows for pi, pj -->
$$
\begin{matrix}
\comm{x_i}{x_j}=0\,, & \comm{p_i}{p_j}=0\,, & \comm{x_i}{p_j} = i\delta_{ij}\hbar\,.
\end{matrix}
$$

Given that $p_x$, $p_y$ and $p_z$ commute, they share a set of simultaneous eigenkets, and thus
$$
\ket{\vb{p'}} = \ket{p_x',p_y',p_z'}
$$
$$
\begin{matrix}
p_x\ket{\vb{p'}} = p_x'\ket{\vb{p'}}\,, &
p_y\ket{\vb{p'}} = p_y'\ket{\vb{p'}}\,, &
p_z\ket{\vb{p'}} = p_z'\ket{\vb{p'}}\,.
\end{matrix}
$$

Finally, let us remark that $\ket{\vb{p'}}$ is an eigenket of $\T{\dd\xp}$:
$$
\begin{aligned}
\T{\dd\xp}\ket{\vb{p'}} &= \left(1-\frac{i\vb{p}\cdot{\dd\xp}}{\hbar}\right)\ket{\vb{p'}}\\
&= \left(1-\frac{i\vb{p'}\cdot{\dd\xp}}{\hbar}\right)\ket{\vb{p'}}
\end{aligned}
$$
<!-- Add hat to all operators! -->