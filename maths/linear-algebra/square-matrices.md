Square Matrices
===============
A square matrix is a matrix with the same number of rows and columns. An $n$-by-$n$ matrix is known as a square matrix of order $n$.

The trace of a square matrix 
$$
\operatorname{tr}(S) = \sum_{i=1}^nS_{ii}
$$
is defined as the sum of its diagonal elements. The trace has the following properties:
* $\operatorname{tr}(AB) = \operatorname{tr}(BA)$
* $\operatorname{tr}(A) = \operatorname{tr}(A^T)$

Classes
-------
There are several classes of square matrix.

### Normal
* Satisfies $U^\dagger U=UU^\dagger$.

### Unitary [Normal]
* Satisfies $UU^\dagger=I$.  
  This implies that $\lvert \det(U)\rvert=1$, as $\lvert UU^\dagger\rvert=\lvert U\rvert\lvert U^\dagger\rvert=\lvert U\rvert^2=1$.
* $U^\dagger=U^{-1}$.
* Only real eigenvalues:
  $$
  \begin{aligned}
  (U\vec{v})^\dagger
  (H^T\vec{v})^\dagger = v^\dagger H &= \bar{\lambda}\vec{v}^\dagger \\
  \vec{v}^\dagger H\vec{v} &= \bar{\lambda}\vec{v}^\dagger\vec{v}
  \end{aligned}
  $$

### Orthogonal [Unitary]
* Satisfies $O^TO=OO^T=I$.
* $O^\dagger=O^{-1}$, therefore $O$ is _real_.
* Orthonormal rows and columns.

### Hermitian [Normal]
* Satisfies $H^\dagger=H$.

### Symmetric [Normal]
* Satisfies $S^T=S$.