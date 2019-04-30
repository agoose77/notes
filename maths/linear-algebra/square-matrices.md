# Square Matrices

A square matrix is a matrix with the same number of rows and columns. An $n$-by-$n$ matrix is known as a square matrix of order $n$.

## Operations

### Trace

The trace of a square matrix is defined as the sum of its diagonal elements,

$$
\operatorname{tr}(S) = \sum_{i=1}^nS_{ii}\,.
$$

It has the following properties:

- $\operatorname{tr}(AB) = \operatorname{tr}(BA)$
- $\operatorname{tr}(A) = \operatorname{tr}(A^T)$

## Classes

There are several classes of square matrix:

### Normal

- Satisfies $U^\dagger U=UU^\dagger$.

### Unitary [Normal]

- Satisfies $UU^\dagger=I$, which implies that $\lvert \det(U)\rvert=1$ (as $\lvert UU^\dagger\rvert=\lvert U\rvert\lvert U^\dagger\rvert=\lvert \det(U)\rvert^2=1$).
- $U^\dagger=U^{-1}$.
- Preserves [inner product](inner-product-space.md)[^1]

  $$
  \begin{aligned}
  \ip{U\vb{u}}{U\vb{v}} &= \vb{v}^\dagger U^\dagger HU\vb{u}\\
  \ip{\vb{u}}{\vb{v}} &= \vb{v}^\dagger H\vb{u}\\
  \ip{U\vb{u}}{U\vb{v}}=\ip{\vb{u}}{\vb{v}}
  &\iff U^\dagger H U = H \\
  &\iff \comm{H}{U} = 0\,, \end{aligned} $$ which holds on an orthonormal basis where $H=I$.
  $$

### Orthogonal [Unitary]

- Satisfies $O^TO=OO^T=I$.
- $O^\dagger=O^{-1}$, therefore $O$ is _real_.
- Orthonormal rows and columns.

### Hermitian [Normal]

- Satisfies $H^\dagger=H$.
- Only real eigenvalues:  
  Let $\vb{v}$ be an eigenvector.
  $$
  \begin{aligned}
  H\vb{v} &= \lambda \vb{v} \\
  \vb{v}^\dagger H\vb{v} &= \lambda \vb{v}^\dagger\vb{v}\\
  \left(\vb{v}^\dagger H\vb{v}\right) = \vb{v}^\dagger H\vb{v} &= \overline{\lambda}\vb{v}^\dagger\vb{v}\\
  \overline{\lambda} &= \lambda \implies \lambda \in \mathbb{R}
  \end{aligned}
  $$
- Orthogonal eigenvectors:  
  Given that $H^*=H^\dagger$[^2], it follows that $\ip{H\vb{u}}{\vb{v}} = \ip{\vb{u}}{H\vb{v}}$. Let $\vb{u}$ and $\vb{v}$ be two eigenvectors (with _real_ nondegenerate eigenvalues). Then,

  $$
  \begin{aligned}
      \ip{H\vb{u}}{\vb{v}} &= \ip{\vb{u}}{H\vb{v}}\\
      \lambda_1\ip{\vb{u}}{\vb{v}} &= \overline{\lambda_2}\ip{\vb{u}}{\vb{v}}\\
      \ip{\vb{u}}{\vb{v}} \left(\lambda_1-\lambda_2\right)&= 0\,,
  \end{aligned}
  $$

  which implies that for _distinct_ eigenvalues,

  $$
    \ip{\vb{u}}{\vb{v}} = 0\,.
  $$

### Symmetric [Normal]

- Satisfies $S^T=S$.

[^1]: When $U$ is defined on an _orthonormal_ basis.
[^2]: $H$ is _only_ self adjoint on an orthonormal basis.
