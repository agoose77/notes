$\gdef\J{\hat{J}}$

# Angular-Momentum Addition

Let us consider two angular-momentum operators $\vb{\J}_1$ and $\vb{\J}_2$ in _different subspaces_. The components of $\vb{\J}_1$ and $\vb{\J}_2$ satisfy the [angular-momentum commutation relations](infinitesimal-rotations.md#Infinitesimal-Rotations-in-Quantum-Mechanics)

$$
\tag{a}
\comm{\J_{ni}}{\J_{nj}} = i\hbar\varepsilon_{ijk}\J_{nk}\,,
$$

where $n\in\{\,1,\,2\,\}$.
Given that $\vb{J}_1$ and $\vb{J}_2$ belong to different subspaces, another commutation relation exists

$$
\tag{b}
\comm{\J^{(1)}_{k}}{\J^{(2)}_{l}} = 0\,.
$$

The [infinitesimal rotation operator](infinitesimal-rotations.md#Infinitesimal-Rotations-in-Quantum-Mechanics) that acts on both subspace 1 and subspace 2 is defined as

$$
\begin{aligned}
\tag{c}
\mathscr{D}_{12}(\vu{n}, \dd\phi) &= \left(1-\frac{i\vb{\J_1}\cdot\vu{n}\dd\phi}{\hbar}\right)\otimes\left(1-\frac{i\vb{\J_2}\cdot\vu{n}\dd\phi}{\hbar}\right)\\
                             &= 1 - \frac{i(\vb{\J_1}\otimes1+1\otimes\vb{\J_2})\cdot\vu{n}\dd\phi}{\hbar}\,.
\end{aligned}
$$

We define the _total_ angular momentum as

$$
\vb{\J} \equiv \vb{\J}_1\otimes1 + 1\otimes\vb{\J}_2=\vb{\J}_1+\vb{\J}_2\,.
$$

The finite rotation form of **(c\)** is

$$
\mathscr{D}_{12}(\vu{n}, \phi) = \exp\mleftright{(}{\frac{i\vb{\J_1}\cdot\vu{n}\phi}{\hbar}}{)}\otimes\exp\mleftright{(}{\frac{i\vb{\J_2}\cdot\vu{n}\phi}{\hbar}}{)}\,,
$$

which also satisfies the angular-momentum commutation relations due to **(a)** and **(b)**, and hence $\vb{\J}$ is an angular momentum. Consequently, the previous understanding of the eigenvalue spectrum of $\vb{\J}^2$ and $\J_z$ also applies to the total $\vb{\J}$.

Clebsch Gordan Coefficients
---------------------------

For the total system, we must choose a set of base kets. There are two possible options:

- Simultaneous eigenkets of $\vb{\J}_1^2$, $\vb{\J}_2^2$, $\J^{(1)}_{z}$, and $\J^{(2)}_{z}$. We may denote these _direct product_ states as $\ket{j_1j_2;m_1m_2}$
  $$
  \begin{aligned}
  \vb{\J}_1^2\ket{j_1,j_2;m_1m_2} &= j_1(j_1+1)\hbar^2\ket{j_1,j_2;m_1m_2}\\
  \J^{(1)}_{z}\ket{j_1,j_2;m_1m_2} &= m_1\hbar\ket{j_1,j_2;m_1m_2}\\
  \vb{\J}_2^2\ket{j_1,j_2;m_1m_2} &= j_2(j_2+1)\hbar^2\ket{j_1,j_2;m_1m_2}\\
  \J^{(2)}_{z}\ket{j_1,j_2;m_1m_2} &= m_2\hbar\ket{j_1,j_2;m_1m_2}\\
  \end{aligned}
  $$
- Simultaneous eigenkets of $\vb{\J}^2$, $\vb{\J}_1^2$, $\vb{\J}_2^2$, and $\J_z$. We may denote these states as $\ket{j_1j_2;jm}$

  $$
  \begin{aligned}
  \vb{\J}_1^2\ket{j_1j_2;jm} &= j_1(j_1+1)\hbar^2\ket{j_1j_2;jm}\\
  \vb{\J}_2^2\ket{j_1j_2;jm} &= j_2(j_2+1)\hbar^2\ket{j_1j_2;jm}\\
  \vb{\J}^2\ket{j_1j_2;jm} &= j(j+1)\hbar^2\ket{j_1j_2;jm}\\
  \J_z\ket{j_1j_2;jm} &= m\hbar\ket{j_1j_2;jm}\\
  \end{aligned}
  $$

We will now drop the explicit labelling of $\J_1$ and $\J_2$ in the state ket: $\ket{j_1j_2;jm}=\ket{jm}$.

Although

$$
      \comm{\vb{\J}^2}{\J^{(1)}_{z}} = 0\,,
$$

it is _not the case_ that the $z$ components of $\vb{\J}_1$ and $\vb{\J}_2$ commute with $\vb{\J}^2$; the two choices for basis kets are not mutually compatible. On the ket space of a given $j_1$ and $j_2$, the identity is

$$
1 = \sum_{m_1m_2}\ket{m_1m_2}\bra{m_1m_2}\,.
$$

Let us also note that by definition,

$$
  (\J_z-\J^{(1)}_{z}-\J^{(2)}_{z})\ket{jm}=0
\,.
$$

Thus it follows for a given $j_1,j_2$ (which are implied for any state $\ket{jm}$) we have

$$
\tag{4}
\begin{aligned}
  \J_z\ket{jm}-(\J^{(1)}_{z}+\J^{(2)}_{z})\ket{jm} &= 0\\
  &= m\hbar\ket{jm}-\sum_{m_1}\sum_{m_2}(\J^{(1)}_{z}+\J^{(2)}_{z})\ket{m_1m_2}\braket{m_1m_2}{jm}\\
  &= m\hbar\ket{jm}-\sum_{m_1}\sum_{m_2}(m_1+m_2)\hbar\ket{m_1m_2}\braket{m_1m_2}{jm}\,.
\end{aligned}
$$

Left multiplying by $\bra{m_1m_2}$, we obtain

$$
\begin{aligned}
  m\hbar\bra{m_1m_2}\ket{jm}-\sum_{m_1'}\sum_{m_2'}(m_1'+m_2')\hbar\bra{m_1m_2}\ket{m_1'm_2'}\braket{m_1'm_2'}{jm} &= 0\\
  m\hbar\braket{m_1m_2}{jm}-(m_1+m_2)\hbar\braket{m_1m_2}{jm} &= 0\\
  \left(m-(m_1+m_2)\right)\hbar\braket{m_1m_2}{jm} &= 0\,,
\end{aligned}
$$

where $\braket{j_1j_2;m_1m_2}{j_1j_2;jm}$ are the Clebsch-Gordan coefficients. From this result it may be deduced that for non-zero coefficients, $$\tag{d}m = m_1 + m_2\,.$$
Consequently, the relation between the two bases is given by **(4)** as 
$$
\ket{jm} = \sum_{m_1}\sum_{m_2}\ket{m_1m_2}\braket{m_1m_2}{jm}\,.
$$

Finding the Relation Between Bases
----------------------------------
Given that the set of base kets $\{\,\ket{jm}\,\}$ is simply a choice of basis, it follows that the dimensionality of the space [should equal](../maths/linear-algebra/vector-space-basis-properties.md#Bases-Have-Same-Dimension) that of the direct product representation. As was demonstrated through the use of ladder operators, there is a top "rung" $m_\text{max}$ given by

$$
\begin{aligned}
    m_\text{max} &= m_{1\,\text{max}}+m_{2\,\text{max}}\\
    &=j_1 + j_2\,,
\end{aligned}
$$

at which $m_\text{max}=j_\text{max}$.

In the direct product representation, for each $j_1,\,j_2$ there are $N=(2j_1+1)\times(2j_2+1)$ possible states. In the total system representation, there are $2j+1$ substates a particular $j$, given by $m=-j,\,-j+1,\,\dots,\,j$. Thus, starting from this top rung we can sum the number of substates for each $j$, until the number of available states $N$ is exhausted:

$$
\begin{aligned}
(2j_1+1)(2j_2+1) &= \sum_{k=0}^K\left(2(j_1+j_2-k)+1\right)\\
                 &= \sum_{k=0}^K\left(2(j_1+j_2)+1\right) -2\sum_{k=0}^Kk\\
                 &= 2(K+1)(j_1+j_2) + (K+1) - 2\frac{K(K+1)}{2}\\
                 &= 2(K+1)(j_1+j_2) + 1 - K^2\,.
\end{aligned}
$$

Solving for $K$,

$$
\begin{aligned}
0 &= K^2 + (2j_1+1)(2j_2+1) - 2(K+1)(j_1+j_2) - 1\\
  &= K^2 - 2K(j_1+j_2) + 4j_1j_2\\
  \\
K &= \frac{2(j_1+j_2) \pm \sqrt{4(j_1+j_2)^2-16j_1j_2}}{2}\\
  &= j_1 + j_2 \pm \sqrt{j_1^2+j_2^2+2j_1j_2-4j_1j_2}\\
  &= j_1 + j_2 \pm \sqrt{(j_1-j_2)^2}\\
  &= 2j_1\text{ or } 2j_2\,.
\end{aligned}
$$

Therefore, the minimal value of $j$ given by $j_\text{min}=j_1+j_2-\min(2j_1,2j_2)$, where $\min$ is used such that the lowering process arrests at the earliest solution. Without knowing a priori $j_1$ and $j_2$, this expression is concisely written as

$$
j_\text{min} = \abs{j_1 - j_2}\,.
$$

One can more explicitly determine these states by acting upon $\ket{jm}$ with the lowering operator $\J_{-}=\J^{(1)}_{{-}}+\J^{(2)}_{-}$, and in each case identify an additional orthogonal state to satisfy the available degrees of freedom.

---

We may conclude that, in the $\ket{jm}$ basis, $j$ and $m$ satisfy $$\abs{j_1-j_2}\leq j\leq j_1+j_2$$ and $$m=m_1 + m_2$$ respectively. The total angular momentum of the _system_ $\vb{\J}$ behaves like an angular momentum, and thus previous work to derive the properties of $\vb{\J}$ still hold.

<!-- TODO recursion relations from Sakurai -->
