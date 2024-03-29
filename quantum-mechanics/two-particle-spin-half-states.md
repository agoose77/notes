# Two Particle Spin-$\frac{1}{2}$ States

$\gdef\S{\hat{S}}$

<!-- TODO, can't we determine this from I = J2 + J2 = L1 + S1 + L2 + S2? -->

Each spin $\frac{1}{2}$ particle can have either $m_s=-\frac{1}{2}$ or $m_s=+\frac{1}{2}$, denoted as $\ket{-}$ and $\ket{+}$ respectively. Hence, in terms of _[direct product](../maths/linear-algebra/tensor-product.md) states_, the total spin state must be one of

$$
\begin{matrix}
\ket{+}_1\otimes\ket{+}_2\\
\ket{-}_1\otimes\ket{+}_2\\
\ket{+}_1\otimes\ket{-}_2\\
\ket{-}_1\otimes\ket{-}_2\\
\end{matrix}
$$

From the [addition rules](angular-momentum-addition.md), in the basis given by the eigenkets of the total operators $\vb{\S}_z$ and $\S$, the $z$ spin projection $m_s$ is given by 
$$
\tag{a}
    m_s=m_s^{(1)} + m_s^{(2)}\,.
$$ 
The total spin $s$ is given by the equality $\abs{s_1-s_2}\leq s\leq s_1+s_2$, which for a spin half system gives $s=0,\,1$. Alongside the [ladder operators](angular-momentum-ladder-operators.md#Ladder-Operators), these relations can be used to find the spin states of our system in each basis.

The Triplet State
-----------------
Given **(a)**, the value of $m_s$ is maximal for the real the direct product state $\ket{+}_1\otimes\ket{+}_2$, where $m_s^{(1)}=m_s^{(2)}=\frac{1}{2}$. The [addition rules](angular-momentum-addition.md) state that the total spin $s$ is equal to the maximal value of $m_s$. It follows that this direct product state corresponds to $\ket{s=1,m_s=1}$ in the new basis. Given that

$$
m_s=-s,\dots,\,s\,,
$$

this state is a _triplet_ state with

$$
m_s=-1,\,\dots 0,\,1\,.
$$

The remaining triplet states can be found in the direct product basis by repeatedly applying the lowering operator to the maximal state $\ket{1,1}$:
| Total State | Direct Product State |
|:----------------: |:----------------------------------------------------------------------------: |
| $\ket{1,\ 1}$ | $\ket{+}_1\otimes\ket{+}_2$ |
| $\ket{1,\ 0}$ | $\frac{1}{\sqrt{2}}\left(\ket{+}_1\otimes\ket{-}_2+\ket{-}_1\otimes\ket{+}_2\right)$ |
| $\ket{1,-1}$ | $\ket{-}_1\otimes\ket{-}_2$ |

Note that all of these states are *symmetric* under particle exchange. 

The Singlet State
-----------------

As we must have the same number of states in either basis, the remaining state is the _singlet_ state $\ket{0,0}$. Like $\ket{1,0}$, it will be a superposition of states (Bell states[^4]) in order for $\S_z=0$ and $\S^2\ket{0,0}=0$. 
One can find the singlet state in the direct product basis by taking the most general state

$$
\ket{0,0} = a\ket{+}_1\otimes\ket{+}_2 + b\ket{+}_1\otimes\ket{-}_2 + c\ket{-}_1\otimes\ket{+}_2 + d\ket{-}_1\otimes\ket{-}_2
$$
and requiring that it satisfy $\S^2\ket{0,0}=0$[^1]. The operator $\S^2$ is given by
$$
\begin{aligned}
\left(\vb{\S^{(1)}} + \vb{\S^{(2)}}\right)\cdot\left(\vb{\S^{(1)}} + \vb{\S^{(2)}}\right)
&={\S^{(1)}}^2 + {\S^{(2)}}^2 + 2\vb{\S^{(1)}}\cdot\vb{\S^{(2)}}\\
&={\S^{(1)}}^2 + {\S^{(2)}}^2 + \S_+^{(1)}\S_-^{(2)} + \S_-^{(1)}\S_+^{(2)}+2\S_z^{(1)}\S_z^{(2)}\,,
\end{aligned}
$$

hence for $\S^2\ket{0,0}$ to be zero,

$$
\begin{matrix}
\frac{3\hbar^2}{2}\left(a\ket{+}_1\otimes\ket{+}_2 + b\ket{+}_1\otimes\ket{-}_2 + c\ket{-}_1\otimes\ket{+}_2 + d\ket{-}_1\otimes\ket{-}_2\right)+\\
\hbar^2\left(c\ket{+}_1\otimes\ket{-}_2\right)+\\
\hbar^2\left(b\ket{-}_1\otimes\ket{+}_2\right)+\\
\frac{\hbar^2}{2}(a\ket{+}_1\otimes\ket{+}_2-b\ket{+}_1\otimes\ket{-}_2-c\ket{-}_1\otimes\ket{+}_2+d\ket{-}_1\otimes\ket{-}_2) = 0
\end{matrix}
$$

which simplifies to

$$
2a\ket{+}_1\otimes\ket{+}_2 +
(b+c)\ket{+}_1\otimes\ket{-}_2 +
(c+b)\ket{-}_1\otimes\ket{+}_2 +
2d\ket{-}_1\otimes\ket{-}_2\,.
$$

This requires $a=d=0$, and $b+c=0$, i.e.

$$
\ket{0,0} = k\left(\ket{+}_1\otimes\ket{-}_2 - \ket{-}_1\otimes\ket{+}_2 \right)\,,
$$

where $k$ is typically taken to be $\frac{1}{\sqrt{2}}$ in order to normalise the state. This result can also be found from the symmetry requirement of the state.[^2][^3] The singlet state is evidently *anti-symmetric* under particle exchange.

<!-- W

TODO why are the sim eigenstates of S^2 and Sz orthogonal (obviously its Hermitian and we know they are orthogonal, but conceptually that is)...
TODO look at entangled states (though not relevant)
-->

[^1]: https://ocw.mit.edu/courses/physics/8-05-quantum-physics-ii-fall-2013/lecture-notes/MIT8_05F13_Chap_08.pdf
[^2]: https://physics.stackexchange.com/a/389957
[^3]: https://physics.stackexchange.com/a/290474
[^4]: https://en.wikipedia.org/wiki/Bell_state
