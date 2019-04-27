# Eigenvectors and Eigenvalues

An eigenvector of a [linear transformation](linear-mapping.md) is a vector whose direction is invariant under that transformation (i.e. it changes only by a scalar factor). More formally, if $T\colon V\rightarrow V$ is a linear transformation from a [vector space](vector-space.md) $V$ over a field $F$ into itself, then $\vec{v}\in V$ is an eigenvector of $T$ if it satisfies

$$
T(\vec{v}) = \lambda\vec{v}\,,
$$

for some $\lambda\in F$.

Given that members of a _finite_ vector space may be represented by a series of coordinates, linear transformations on these spaces may be represented by [square matrices](square-matrices.md) (as they transform between the same basis vectors) which act upon column vectors of space coordinates.

## Matrices

In matrix form, an eigenvector of some linear transformation $T$ may be written as

$$
\tag{a}
A\vec{v} = \lambda \vec{v}\,,
$$

where $A$ is the square matrix representing $T$. This equation has a non-zero solution $\iff$ the determinant of the matrix $A-\lambda I$ is zero[^1], hence eigenvalues of $A$ must satisfy

$$
\lvert \tag{b} A-\lambda I\rvert=0\,.
$$

<!-- If Mx = 0 is to have a nontrivial solution, then the columns of M must be linearly dependent, i.e. M must have det(M)=0.-->

Eq. **(b)** is a polynomial of degree $n=\det(A)$, called the _characteristic polynomial_ of A, which may be factored into the product of $n$ linear terms,

$$
\tag{c}
\lvert A-\lambda I\rvert = (\lambda_1-\lambda)(\lambda_2-\lambda)\dots(\lambda_n-\lambda)\,.
$$

Once the eigenvalues $\{\,\lambda_i\,\}$ have been found, Eq. **(a)** may be solved for $\vec{v_\lambda}$.

<!-- Link properties of trace of A == sum of eigenvalues (similarity transform link)
Determimant = prod of eigenvalues
-->

[^1]: http://mathworld.wolfram.com/InvertibleMatrixTheorem.html "Invertible Matrix Theorem"
