Square Matrices
===============
A square matrix is a matrix with the same number of rows and columns. An $n$-by-$n$ matrix is known as a square matrix of order $n$.

Operations
-----------
### Trace
The trace of a square matrix is defined as the sum of its diagonal elements,
$$
\operatorname{tr}(S) = \sum_{i=1}^nS_{ii}\,.
$$
It has the following properties:
  * $\operatorname{tr}(AB) = \operatorname{tr}(BA)$
  * $\operatorname{tr}(A) = \operatorname{tr}(A^T)$

Classes
-------
There are several classes of square matrix:

### Normal
* Satisfies $U^\dagger U=UU^\dagger$.

### Unitary [Normal]
* Satisfies $UU^\dagger=I$, which implies that $\lvert \det(U)\rvert=1$ (as $\lvert UU^\dagger\rvert=\lvert U\rvert\lvert U^\dagger\rvert=\lvert \det(U)\rvert^2=1$).
* $U^\dagger=U^{-1}$.
* Preserves *standard* inner product
  <!-- TODO -->
  $$
  \begin{aligned}
      \ip{U\vb{v}}{U\vb{w}} &= \vb{u}^TU^TH\overline{U}\overline{\vb{v}}\\
      \ip{\vb{v}}{\vb{w}} &= \vb{u}^TH\overline{\vb{v}}\\
      \ip{U\vb{v}}{U\vb{w}}=\ip{\vb{v}}{\vb{w}} &\iff (U^TH\overline{U})^T = H^T \\
                                                &\iff U^\dagger H U = H\\
                                                &\iff \comm{H}{U} = 0\,,
  \end{aligned}
  $$
  where $\comm{H}{U} = 0$ holds, given that $H=I$ on the standard basis.

### Orthogonal [Unitary]
* Satisfies $O^TO=OO^T=I$.
* $O^\dagger=O^{-1}$, therefore $O$ is _real_.
* Orthonormal rows and columns.

### Hermitian [Normal]
* Satisfies $H^\dagger=H$.
* Only real eigenvalues:
  $$
  \begin{aligned}
  (U\vb{v})^\dagger
  (H^T\vb{v})^\dagger = v^\dagger H &= \bar{\lambda}\vb{v}^\dagger \\
  \vb{v}^\dagger H\vb{v} &= \bar{\lambda}\vb{v}^\dagger\vb{v}
  \end{aligned}
  $$

### Symmetric [Normal]
* Satisfies $S^T=S$.