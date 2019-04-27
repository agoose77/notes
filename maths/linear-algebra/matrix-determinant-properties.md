# Matrix Determinant Properties

## The Determinant

$$
    \lvert A \rvert  = \sum_{i=1}^ka_{ij}C_{ij}\,,
$$

- $C_{ij}=(-1)^{i+j}M_{ij}$ is the cofactor matrix.
- $M_{ij}$ is the minor matrix of $A$, made by eliminating row $i$ and column $j$.

## Multiplication by Scalar

$$
    \lvert cA\rvert=c^n\lvert A\rvert\,,
$$

From this it follows that
$$\lvert {-A}\rvert=(-1)^n\lvert A\rvert\,.$$

## Matrix Product

$$
\lvert AB \rvert = \lvert A \rvert\lvert B\rvert\,.
$$

This relation may be used to determine $\lvert A^{-1}\rvert$,

$$
\begin{aligned}
\lvert I \rvert = 1 &= \lvert A A^{-1}\rvert\\
&= \lvert A\rvert\lvert A^{-1}\rvert\\
\frac{1}{\lvert A\rvert} &= \lvert A^{-1}\rvert \,.
\end{aligned}
$$

## Complex Conjugate

$$
\lvert A^\ast\rvert = \lvert A \rvert^\ast\,.
$$

## Elementary Row / Column Operations

|         Operation         | Effect upon Determinant $D$ |
| :-----------------------: | :-------------------------: |
| $r_i\leftrightarrow r_j$  |            $-D$             |
|   $r_i\rightarrow ar_i$   |            $aD$             |
| $r_i\rightarrow r_i+cr_j$ |             $D$             |

## Linear Dependence

Where $A$ has linearly dependent rows or columns, $\lvert A\rvert=0$. See the [Invertible Matrix Theorem](http://mathworld.wolfram.com/InvertibleMatrixTheorem.html).
