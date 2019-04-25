Angular-Momentum Eigenvalues
============================
<!--  of $\J^2$ and $\J_z$ -->
$\gdef\J{\hat{J}}$
It can be shown for Hermitian operators that the eigenvalues are *real*, and the eigenvectors *orthogonal*. By convention, we take the *normalised* eigenkets such that they form an *orthonormal set* $\set{\ket{a'}}$. It is assumed that the eigenkets span the entire ket space.
<!-- TODO show that they span the space -->
It was shown that one can generate eigenkets of $\J^2$ and $\J_z$ using the [ladder operators](angular-momentum-ladder-operators.md) to raise or lower $b$. It can be shown that there exists an upper bound to $b$ for a given $a$. First, we note that
$$
\begin{aligned}
\J^2 - \J_z 
&= \J_x^2 + \J_y^2 = \J_+\J_- - i\comm{\J_y}{\J_x}\\
&= \J_+\J_- - \hbar\J_z\\
&= \J_+\J_- - \frac{1}{2}\comm{\J_+}{\J_-}\\
&= \frac{1}{2}\left(\J_+\J_- + \J_-\J_+\right)\,.
\end{aligned}
$$
Given that $\J_i$ are hermitian, it follows that $\J_\pm=\J_\mp^\dagger$, hence
$$
\J^2 - \J_z = \frac{1}{2}\left(\J_+\J_+^\dagger + \J_-\J_-^\dagger\right)\,.
$$
Taking the expectation value of $\J^2 - \J_z$, we see that
$$
\begin{aligned}
\expval{\J^2 - \J_z} 
&= \frac{1}{2}\bra{a,b}\left(\J_+\J_+^\dagger + \J_-\J_-^\dagger\right)\ket{a,b}\\
&=\frac{1}{2}\left(\bra{a,b}\J_+\J_+^\dagger\ket{a,b} + \bra{a,b}\J_-\J_-^\dagger\ket{a,b}\right)\,.
\end{aligned}
$$
From the positive definiteness $\braket{v}{v}\geq 0$ of the [inner product](../maths/linear-algebra/inner-product-space.md#The-Inner-Product) it follows that both inner products are non-negative, and thus $\expval{\J^2 - \J_z}\geq 0$. This expression implies 
$$
\tag{d}
a \geq b\,.
$$
A question therefore arises; what should happen at the top rung?[^1] One might suppose that $\J_+\ket{a,b_\text{max}}=\gamma\ket{a,b_\text{max}}$. If so, let us revisit **(c\)**
$$
\def\bm{b_\text{max}}
\begin{aligned}
\J_z\left(\J_+\ket{a,\bm}\right) 
&= \left(\comm{\J_z}{\J_+} + \J_+\J_z\right)\ket{a,\bm}\\
&= \left(\hbar \J_+ + \J_+\J_z\right)\ket{a,\bm}\\
&= \left(\gamma\hbar + \gamma\hbar\bm\right)\ket{a,\bm}\\
&= \gamma\hbar\left(1 + \bm\right)\ket{a,\bm}\,.
\end{aligned}
$$
However, by direct calculation,
$$
\def\bm{b_\text{max}}
\J_z\left(\J_+\ket{a,\bm}\right) = \gamma\hbar\bm\ket{a,\bm}\,.
$$
These two results agree only if $\gamma=0$, and thus 
$$
\tag{e}
\J_+\ket{a,b_\text{max}} = 0\,.
$$

Given **(e)** it follows that
$$
\tag{f}
\begin{aligned}
\J_-\J_+\ket{a,b_\text{max}} 
&= 0\\
&= \J^2 -\J_z^2 - \hbar \J_z\,,
\end{aligned}
$$
so 
$$
\left(\J^2 -\J_z^2 - \hbar \J_z\right)\ket{a,b_\text{max}} = 0\,.
$$
As $\ket{a,b_\text{max}}$ is not a null ket, it follows that 
$$
\tag{g}
\def\bm{b_\text{max}}
a - \bm^2-\bm\hbar = 0 \implies a = \bm(\bm+\hbar)\,.
$$
From **(d)** there must also be some $b_\text{min}$ for which 
$$
\J_-\ket{a,b_\text{min}}=0\,.
$$
Using the same approach as **(f)**, we may write $\J_+\J_-$ as 
$$
\J_+\J_- = \J^2 -\J_z^2 + \hbar \J_z
$$
to find
$$
\tag{h}
\def\bm{b_\text{min}}
a = \bm(\bm-\hbar).
$$
The expressions in **(g)** and **(h)** imply that $b_\text{min}=-b_\text{max}$. Given that an application of the ladder operators varies $b$ by $\pm\hbar$, it follows that 
$$
b = b_\text{min} + n\hbar \implies b_\text{max}=\frac{n\hbar}{2}\,.
$$
Letting $j=\frac{b_\text{max}}{\hbar}$, we may write **(g)** as
$$
a = \hbar^2j(j+1)\,.
$$
As $b$ is symmetric about $0$, we may also define $m$ such that 
$$
b \equiv m\hbar\,.
$$
Evidently, for a given $j$ we have $2j+1$ permitted values of $m$, from $m=-j$ to $m=+j$. It is often more convenient to use this notation to denote a simultaneous eigenket of $\J^2$ and $\J$ as $\ket{j,m}$ such that
$$
\begin{aligned}
\J^2\ket{j,m} &= j(j+1)\hbar^2\ket{j,m}\\
\J_z\ket{j,m} &= m\hbar\ket{j,m}\,.
\end{aligned}
$$

Finding $c_\pm$ for $\J_\pm$
-----------------------------
In defining the ladder operators $\J_\pm$, it was noted that 
$$
\J_\pm\ket{j,m} = c_\pm\ket{j,m\pm1}\,.
$$
In order to find $c_\pm$, let us take the inner product of some state $\J_\pm\ket{j,m}$ with itself, where $\ket{j,m}$ is normalised:
$$
\begin{aligned}
\bra{j,m}\J_\pm^\dagger\J_\pm\ket{j,m} =\abs{\J_\pm\ket{j,m}}^2
&= \bra{j,m}\J^2-\J_z^2\mp\hbar\J_z\ket{j,m}\\
&= \left(j(j+1) - m^2 \mp m\right)\hbar^2\,.
\end{aligned}
$$
<!-- TODO link to phase factor is arbitrary -->
Taking $c_\pm$ as real positive (as the phase factor is arbitrary), $\J_\pm$ is defined as
$$
\J_\pm\ket{j,m} = \hbar\sqrt{j(j+1) - m^2 \mp m}\ket{j,m\pm1}\,.
$$

[^1]: https://physics.stackexchange.com/questions/179532/why-does-the-raising-operator-when-acting-on-a-ket-with-a-maximum-second-quantu