Matrix Representation
=====================
<!-- TODO: field -->
The complex numbers are the [field](field.md) $\mathbb{C}$ of numbers of the form $x+\mathbf{i}\,y$ where $x,y$ denote real numbers, and $\mathbf{i}$ is the imaginary unit which satisfies $\mathbf{i}^2=-1$. 
$\mathbb{C}$ can be represented in terms of matrices. Consider the matrix $\mathbf{M}$ of the form
$$
\mathbf{M} = \begin{bmatrix}
a & -b \\ 
b & a
\end{bmatrix}\,.
$$

Such a matrix decomposes into
$$
\begin{aligned}
\mathbf{M} &= a\begin{bmatrix}
1 & 0 \\ 
0 & 1
\end{bmatrix} + b\begin{bmatrix}
0 & -1 \\ 
1 & 0
\end{bmatrix}\\
&=a\mathbb{I}+b\mathbf{J}\,,
\end{aligned}
$$
where the matrix $\mathbf{J}=\begin{bmatrix}0 & -1\\1 & 0 \end{bmatrix}$ has the property $\mathbf{J}^2=-\mathbb{I}$. In order for this to be a true representation of $\mathbb{C}$, the set $\mathbb{C}'$ of all $\mathbf{M}$ given by $\set{a\mathbb{I}+b\mathbf{J}:a,b\in \mathbb{R}}$ alongside the matrix addition $(\cdot+\cdot)$ and multiplication $(\cdot\times\cdot)$ operators must satisfy the field axioms. 

The following field axioms are satisfied by any matrix:
* Distributivity of multiplication over addition
* Additive inverses
* Additive and multiplicative identity
* Commutativity of addition
* Associativity of addition and multiplication.

Whcih leaves two additional axioms:
* Multiplicative inverses
* Commutivity of multiplication.

Commutativity of multiplication follows from the fact that $\mathbf{J}^2$ and $\mathbb{I}\mathbf{J}$ are commutative. The multiplicative inverse can be found after considering $\mathbf{M}\times\mathbf{M}^T$, which is equal to 
$$
\begin{aligned}
\mathbf{M}\times\mathbf{M}^T 
&= \begin{bmatrix}
a & -b \\ 
b & a
\end{bmatrix}\begin{bmatrix}
a & b \\ 
-b & a
\end{bmatrix}\\
&=(a^2+b^2)\begin{bmatrix}
1 & 0 \\ 
0 & 1
\end{bmatrix}\\
&=(a^2+b^2)\mathbb{I}\,,
\end{aligned}
$$
i.e. 
$$
\mathbf{M}^{-1} = \frac{1}{(a^2+b^2)}\mathbf{M}^T\,.
$$

It follows that $\mathbb{C}'$ is a (matrix) *representation* of $\mathbb{C}$.