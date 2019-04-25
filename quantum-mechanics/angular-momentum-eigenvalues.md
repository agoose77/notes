Angular Momentum Eigenvalues
============================
$\gdef\J{\hat{J}}$
Ladder Operators
----------------
Let us define the operator $\J^2 \equiv  \vb{\J}\cdot \vb{\J}$, that is $\J^2 \equiv \J_x\J_x + \J_y\J_y + \J_z\J_z$.
<!-- TODO link proofs on common eigenbases -->
Using the [fundamental commutation relations](infinitesimal-rotations.md#Infinitesimal-Rotations-in-Quantum-Mechanics) and cyclical permutation, it can be shown that $\hat{J}^2$ commutes, and thus shares a common eigenbasis with, every one of $\J_i$, i.e.
$$
    \tag{a}
    \comm{\J^2}{\J_i} = 0
$$
Consider $\J_z$:
$$
\begin{aligned}
\comm{\J_x\J_x + \J_y\J_y + \J_z\J_z}{\J_z} 
&= \J_x\comm{\J_x}{\J_z} + \comm{\J_x}{\J_z}\J_x + \J_y\comm{\J_y}{\J_z} + \comm{\J_y}{\J_z}\J_y\\
&= -i\hbar \J_x\J_y  - i\hbar\J_y\J_x + i\hbar \J_y\J_x + i\hbar \J_x\J_y\\
&= 0\,.
\end{aligned}
$$
<!-- TODO link notes on simultaneous diagonalisation -->
Given that the angular momentum operators do not *mutually* commute, we can choose only one of them to be diagonalised simultaneously (share a set of eigenstates) with $\J^2$. By convention, let us choose $\J_z$. We may denote the eigenvalues of $\J^2$ and $\J_z$ by $a$ and $b$, respectively:
$$
\begin{aligned}
\J^2\ket{a,b} &= a\ket{a,b}\\
\J_z\ket{a,b} &= b\ket{a,b}\,.
\end{aligned}
$$

In order to determine the permitted values for $a$ and $b$, one may introduce the non-Hermitian operators
$$
\J_\pm \equiv \J_x \pm i\J_y\,.
$$
These operators satisfy the commutation relations
$$
\tag{b}
\begin{aligned}
    \comm{\J_+}{\J_-} &= 2\hbar \J_z\\
    \comm{\J_z}{\J_\pm} &= \pm\hbar \J_\pm\\
    \comm{\J^2}{\J_\pm} &= 0
    \,,
\end{aligned}
$$
which follows from the fundamental commutation relations and **(a)**. 

It is interesting to observe how $\J_z$ acts upon $\J_\pm\ket{a,b}$
$$
\tag{c}
\begin{aligned}
\J_z\left(\J_\pm\ket{a,b}\right) 
&= \left(\comm{\J_z}{\J_\pm} + \J_\pm\J_z\right)\ket{a,b}\\
&= \left(b\pm\hbar\right)\J_\pm\ket{a,b}\,.
\end{aligned}
$$
Evidently, given an eigenket $\ket{a,b}$ of $\J_z$, the state $\J_\pm\ket{a,b}$ is *also* an eigenket, with eigenvalue $b\pm\hbar$. It is for this reason that $\J_\pm$ are called the *ladder operators*. Similarly, given **(b)** $\ket{a,b}$ is also an eigenket of $\J^2$ and thus we may write
$$
\J_\pm\ket{a,b} = c_\pm\ket{a,b\pm\hbar}\,,
$$
where $c_\pm$ is an arbitrary proportionality constant to be chosen later. 
<!-- TODO link to proof that the set of eigenkets {J+/-|a,b>} is the same as that of {|a,b>}. -->

Eigenvalues of $\J^2$ and $\J_z$
--------------------------------
It can be shown for Hermitian operators that the eigenvalues are *real*, and the eigenvectors *orthogonal*. By convention, we take the *normalised* eigenkets such that they form an *orthonormal set* $\set{\ket{a'}}$. It is assumed that the eigenkets span the entire ket space.
<!-- TODO show that they span the space -->
Above it was shown that one can generate eigenkets of $\J^2$ and $\J_z$ using the ladder operators to raise or lower $b$. It can be shown that there exists an upper bound to $b$ for a given $a$. First, we note that
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
\J_+\ket{a,b_\text{max}} = 0\,.
$$

[^1]: https://physics.stackexchange.com/questions/179532/why-does-the-raising-operator-when-acting-on-a-ket-with-a-maximum-second-quantu