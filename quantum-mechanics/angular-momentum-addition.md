$\gdef\J{\hat{J}}$

Angular-Momentum Addition
=========================

Let us consider two angular-momentum operators $\vb{\J}_1$ and $\vb{\J}_2$ in *different subspaces*. The components of $\vb{\J}_1$ and $\vb{\J}_2$ satisfy the angular-momentum commutation relations
$$
\tag{a}
\comm{\J_{ni}}{\J_{nj}} = i\hbar\varepsilon_{ijk}\J_{nk}\,,
$$
where $n\in\{\,1,\,2\,\}$.
Given that $\vb{J}_1$ and $\vb{J}_2$ belong to different subspaces, another commutation relation exists
$$
\tag{b}
\comm{\J_{1k}}{\J_{2l}} = 0\,.
$$
The infinitesimal rotation operator that acts on both subspace 1 and subspace 2 is defined as
$$
\begin{aligned}
\tag{c}
\mathscr{D}_{12}(\vu{n}, \dd\phi) &= \left(1-\frac{i\vb{\J_1}\cdot\vu{n}\dd\phi}{\hbar}\right)\otimes\left(1-\frac{i\vb{\J_2}\cdot\vu{n}\dd\phi}{\hbar}\right)\\
                             &= 1 - \frac{i(\vb{\J_1}\otimes1+1\otimes\vb{\J_2})\cdot\vu{n}\dd\phi}{\hbar}\,.
\end{aligned}
$$
We define the *total* angular momentum as
$$
\vb{\J} \equiv \vb{\J}_1\otimes1 + 1\otimes\vb{\J}_2=\vb{\J}_1+\vb{\J}_2\,.
$$
The finite rotation form of **(c\)** is 
$$
\mathscr{D}_{12}(\vu{n}, \phi) = \exp\mleftright{(}{\frac{i\vb{\J_1}\cdot\vu{n}\phi}{\hbar}}{)}\otimes\exp\mleftright{(}{\frac{i\vb{\J_2}\cdot\vu{n}\phi}{\hbar}}{)}\,,
$$
which also satisfies the angular-momentum commutation relations due to **(a)** and **(b)**, and hence $\vb{\J}$ is an angular momentum. Consequently, the previous understanding of the eigenvalue spectrum of $\vb{\J}^2$ and $\J_z$ also applies to the total $\vb{\J}$.

For the total system, we must choose a set of base kets. There are two possible options:
* Simultaneous eigenkets of $\vb{\J}_1^2$, $\vb{\J}_2^2$, $\J_{1z}$, and $\J_{2z}$. We may denote these _direct product_ states as $\ket{j_1j_2;m_1m_2}$
  $$
  \begin{aligned}
  \vb{\J}_1^2\ket{j_1,j_2;m_1m_2} &= j_1(j_1+1)\hbar^2\ket{j_1,j_2;m_1m_2}\\
  \J_{1z}\ket{j_1,j_2;m_1m_2} &= m_1\hbar\ket{j_1,j_2;m_1m_2}\\
  \vb{\J}_2^2\ket{j_1,j_2;m_1m_2} &= j_2(j_2+1)\hbar^2\ket{j_1,j_2;m_1m_2}\\
  \J_{2z}\ket{j_1,j_2;m_1m_2} &= m_2\hbar\ket{j_1,j_2;m_1m_2}\\
  \end{aligned}
  $$
* Simultaneous eigenkets of $\vb{\J}^2$, $\vb{\J}_1^2$, $\vb{\J}_2^2$, and $\J_z$. We may denote these states as $\ket{j_1j_2;jm}$
  $$
  \begin{aligned}
  \vb{\J}_1^2\ket{j_1j_2;jm} &= j_1(j_1+1)\hbar^2\ket{j_1j_2;jm}\\
  \vb{\J}_2^2\ket{j_1j_2;jm} &= j_2(j_2+1)\hbar^2\ket{j_1j_2;jm}\\
  \vb{\J}^2\ket{j_1j_2;jm} &= j(j+1)\hbar^2\ket{j_1j_2;jm}\\
  \J_z\ket{j_1j_2;jm} &= m\hbar\ket{j_1j_2;jm}\\
  \end{aligned}
  $$
  
Although 
$$
      \comm{\vb{\J}^2}{\J_{1z}} = 0\,,
$$
it is not the case that the $z$ components of $\vb{\J}_1$ and $\vb{\J}_2$ commute with $\vb{\J}^2$, and thus the two choices for basis kets are not mutually compatible. We will now drop the explicit labelling of $\J_1$ and $\J_2$ in the state ket: $\ket{j_1j_2;jm}=\ket{jm}$

On the ket space of a given $j_1$ and $j_2$, the identity to reconstruct any state (for a given $j_1,j_2$) is
$$
1 = \sum_{m_1m_2}\ket{j_1j_2;m_1m_2}\bra{j_1j_2;m_1m_2}\,.
$$
Let us also note that by definition, 
$$
  (\J_z-\J_{1z}-\J_{2z})\ket{jm}=0
\,.
$$
Thus it follows
$$
\begin{aligned}
  \J_z\ket{jm}-(\J_{1z}+\J_{2z})\ket{jm} &= 0\\
  &= m\hbar\ket{jm}-\sum_{m_1}\sum_{m_2}(\J_{1z}+\J_{2z})\ket{m_1m_2}\braket{j_1j_2;m_1m_2}{j_1j_2;jm}\\
  &= m\hbar\ket{jm}-\sum_{m_1}\sum_{m_2}(m_1+m_2)\hbar\ket{m_1m_2}\braket{j_1j_2;m_1m_2}{j_1j_2;jm}\,.
\end{aligned}
$$
Left multiplying by $\bra{j_1j_2;m_1m_2}$, we obtain
$$  
\begin{aligned}
  m\hbar\bra{j_1j_2;m_1m_2}\ket{jm}-\sum_{m_1'}\sum_{m_2'}(m_1'+m_2')\hbar\bra{m_1m_2}\ket{m_1'm_2'}\braket{j_1j_2;m_1'm_2'}{j_1j_2;jm} &= 0\\
  m\hbar\braket{j_1j_2;m_1m_2}{j_1j_2;jm}-(m_1+m_2)\hbar\braket{j_1j_2;m_1m_2}{j_1j_2;jm} &= 0\\
  \left(m-(m_1+m_2)\right)\hbar\braket{j_1j_2;m_1m_2}{j_1j_2;jm} &= 0\,,
\end{aligned}
$$
where $\braket{j_1j_2;m_1m_2}{j_1j_2;jm}$ are the Clebsch-Gordan coefficients. From this result it may be deduced that for non-zero coefficients, $$\tag{d}m = m_1 + m_2\,.$$

Given that the set of base kets $\{\,\ket{jm}\,\}$ is simply a choice of basis, it follows that the dimensionality of the space [should equal](../maths/linear-algebra/vector-space-basis-properties.md#Bases-Have-Same-Dimension) that of the direct product representation. As was demonstrated through the use of ladder operators, there is a top "rung" given by 
$$
\begin{aligned}
    m_\text{max} =j &= m_{1\,\text{max}}+m_{2\,\text{max}}\\
    &=j_1 + j_2
\end{aligned}
$$ (from **(d)**). For each $j$, we can apply the lowering operator $\J_{-}=\J_{1\,{-}}+\J_{1\,{-}}$

In the direct product representation, for each $j_1,\,j_2$ there are $(2j_1+1)\times(2j_2+1)$ possible states.
<!-- 222 -->
<!-- see 196 -->
